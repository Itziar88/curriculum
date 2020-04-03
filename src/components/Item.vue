<template>
    <div class="Item">
        <div class="WrapperTitle">
            <div class="Simbol"/>
            <CText
                typo="h3"
                class="Title"
            >
                {{ title }}
            </CText>
        </div>
        <div class="CenterDates">
            <CText
                typo="h5"
                weight="semi"
            >
                {{ center }}
            </CText>
            <div class="Dates">
                <CText
                    typo="h6"
                    weight="semi"
                    color="grey01"
                >
                    {{ startDate }}
                </CText>
                <span> - </span>
                <CText
                    typo="h6"
                    weight="semi"
                    color="grey01"
                >
                    {{ endDate }}
                </CText>
            </div>
        </div>
        <CText
            v-if="description"
            align="justify"
            class="Description"
        >
            {{ description }}
        </CText>
    </div>
</template>

<script>
import { CText } from '@/components'
import VueTypes from 'vue-types'

export default {
    name: 'Item',
    components: {
        CText,
    },
    props: {
        title: VueTypes.string,
        center: VueTypes.string,
        startDate: VueTypes.string,
        endDate: VueTypes.string,
        description: VueTypes.string,
    }
}
</script>

<style lang="scss" scoped>
@import '@/theme/theme.scss';

.Item {
    margin-bottom: $spacer * 2;
}
.Simbol {
    height: 5px;
    width: 5px;
    margin-right: 7px;
    border-right: 3px solid $primary;
    border-top: 3px solid $primary;
    transform: rotate(45deg);
}
.WrapperTitle {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    .Title {
        width: 100%;
        border-bottom: 1px solid $black;
    }
}
.CenterDates,
.Description {
    padding-left: $spacer;
}
.CenterDates {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 10px 0px 5px 0px;
}
.Dates {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    span {
        padding: 0px 5px;
    }
}
</style>