<template>
  <div class="Sidebar">
    <div class="Info">
      <img :src="foto" class="Image" />
      <CText
        typo="h3"
        weight="semi"
        align="center"
      >
        {{ name }}
      </CText>
      <CText
        typo="h4"
        weight="medium"
        italic
      >
        {{ job }}
      </CText>
    </div>
    <Contact :info="contact" />
    <Technologies :info="technologies" />
    <Languages :info="languages" />
  </div>
</template>

<script>
import foto from "@/assets/foto.jpg";
import { CText } from "@/components";
import { Contact, Technologies, Languages } from "@/sections";
import VueTypes from "vue-types";

export default {
  name: "Sidebar",
  components: {
    Contact,
    Technologies,
    Languages,
    CText
  },
  props: {
    name: VueTypes.string,
    job: VueTypes.string,
    contact: VueTypes.array,
    technologies: VueTypes.array,
    languages: VueTypes.array
  },
  data() {
    return { foto };
  }
};
</script>

<style lang="scss" scoped>
@import "@/theme/theme.scss";

.Sidebar {
  width: 100%;
  height: 100%;
  background-color: $secondary;
  .Contact,
  .Technologies,
  .Languages {
    margin-top: $spacer * 3;
  }
}

.Info {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0px -15px $spacer * 3 -15px;
  padding-bottom: $spacer;
  border-bottom: 1px dotted $black;
  .CText {
    margin-bottom: 7px;
  }
}
.Image {
  width: 150px;
  height: 150px;
  margin-bottom: $spacer;
  border-radius: 100%;
  border: 3px solid $primary;
}
</style>
