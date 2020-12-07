<template>
  <div id="app" class="Container">
    <Sidebar
      :name="cv.name"
      :job="cv.job"
      :contact="cv.contact"
      :technologies="cv.technologies"
      :languages="cv.languages"
    />
    <div class="Body">
      <Experience :experiences="cv.experience" />
      <Education :studies="cv.studies" />
    </div>
  </div>
</template>

<script>
import { default as cv } from "./cv_en";

import { Sidebar, Experience, Education } from "./sections";

export default {
  name: "App",
  components: {
    Sidebar,
    Experience,
    Education
  },
  data() {
    return {
      cv
    };
  }
};
</script>

<style lang="scss" scoped>
@import "@/theme/theme.scss";

.Container {
  display: flex;
  position: relative;
  box-sizing: border-box;
  min-height: calc(100vh);
  @media print {
    -webkit-print-color-adjust: exact;
    height: calc(100vh);
  }

  .Sidebar,
  .Body {
    padding: $spacer * 2 $spacer;
  }

  .Sidebar {
    flex: 1 1 25%;
  }
  .Body {
    flex: 1 1 75%;
    .Education {
      margin-top: $spacer * 2;
    }
  }
}
</style>
