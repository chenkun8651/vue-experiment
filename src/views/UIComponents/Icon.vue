<template>
  <div class="flex" ref="box">
    <!-- 图标 -->
    <div class="w-9/12">
      <!-- AntDesignVue -->
      <a-card id="1" class="my-5" title="AntDesignVue 图标">
        <div class="w-full flex flex-row flex-wrap justify-start items-center">
          <div class="my-2 mr-5">
            <span class="mr-2">是否开启旋转动画</span>
            <a-switch v-model="AntDesignVue.spin" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标类型</span>
            <el-select size="small" class="w-36" v-model="AntDesignVue.theme">
              <el-option :value="'filled'">filled</el-option>
              <el-option :value="'outlined'">outlined</el-option>
              <el-option :value="'twoTone'">twoTone</el-option>
            </el-select>
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标名称</span>
            <a-input class="w-36" v-model="AntDesignVue.type" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标大小</span>
            <a-input-number class="w-24" v-model="AntDesignVue.fontSize" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置实心（描线）图标颜色</span>
            <a-input class="w-24" v-model="AntDesignVue.color" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置双色图标颜色</span>
            <a-input class="w-24" v-model="AntDesignVue.twoToneColor" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标初始旋转角度</span>
            <a-input-number class="w-24" v-model="AntDesignVue.rotate" />
          </div>
        </div>
        <div>
          <a-icon
            :style="{
              fontSize: `${AntDesignVue.fontSize}px`,
              color: `${AntDesignVue.color}`,
            }"
            :type="AntDesignVue.type"
            :theme="AntDesignVue.theme"
            :spin="AntDesignVue.spin"
            :rotate="AntDesignVue.rotate"
            :two-tone-color="AntDesignVue.twoToneColor"
          >
          </a-icon>
        </div>
        <div>
          <span>自定义图标</span>
          <HeartIcon
            class="m-1.5"
            :style="{
              fontSize: `${AntDesignVue.fontSize}px`,
              color: `${AntDesignVue.color}`,
            }"
          />
          <PandaIcon
            class="m-1.5"
            :style="{
              fontSize: `${AntDesignVue.fontSize}px`,
              color: `${AntDesignVue.color}`,
            }"
          />
          <span class="ml-10">
            <a target="_blank" href="http://iconfont.cn/">iconfont.cn</a>
            图标库图标
          </span>
          <IconFont
            class="m-1.5"
            type="icon-facebook"
            :style="{
              fontSize: `${AntDesignVue.fontSize}px`,
              color: `${AntDesignVue.color}`,
            }"
          />
          <IconFont
            class="m-1.5"
            type="icon-twitter"
            :style="{
              fontSize: `${AntDesignVue.fontSize}px`,
              color: `${AntDesignVue.color}`,
            }"
          />
        </div>
      </a-card>
      <!-- ElementUI -->
      <a-card id="2" class="my-5" title="ElementUI 图标">
        <div class="w-full flex flex-row flex-wrap justify-start items-center">
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标名称</span>
            <a-input class="w-36" v-model="ElementUI.class" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标大小</span>
            <a-input-number class="w-24" v-model="ElementUI.fontSize" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标颜色</span>
            <a-input class="w-24" v-model="ElementUI.color" />
          </div>
        </div>
        <div>
          <i
            :style="{
              fontSize: `${ElementUI.fontSize}px`,
              color: `${ElementUI.color}`,
            }"
            :class="ElementUI.class"
          >
          </i>
        </div>
      </a-card>
      <!-- AtUI -->
      <a-card id="3" class="my-5" title="AtUI 图标">
        <div class="w-full flex flex-row flex-wrap justify-start items-center">
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标名称</span>
            <a-input class="w-36" v-model="AtUI.class" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标大小</span>
            <a-input-number class="w-24" v-model="AtUI.fontSize" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标颜色</span>
            <a-input class="w-24" v-model="AtUI.color" />
          </div>
        </div>
        <div>
          <i
            :style="{ fontSize: `${AtUI.fontSize}px`, color: `${AtUI.color}` }"
            :class="AtUI.class"
          >
          </i>
        </div>
      </a-card>
      <!-- ViewUI -->
      <a-card id="4" class="my-5" title="ViewUI 图标">
        <div class="w-full flex flex-row flex-wrap justify-start items-center">
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标名称</span>
            <a-input class="w-36" v-model="ViewUI.type" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标大小</span>
            <a-input-number class="w-36" v-model="ViewUI.size" />
          </div>
          <div class="my-2 mr-5">
            <span class="mr-2">设置图标颜色</span>
            <a-input class="w-36" v-model="ViewUI.color" />
          </div>
        </div>
        <div>
          <Icon :type="ViewUI.type" :size="ViewUI.size" :color="ViewUI.color">
          </Icon>
        </div>
      </a-card>
    </div>
    <BasicAnchor
      :parentList="this.AnchorInfo.iconAnchor"
      :parentRefs="this.$refs"
    >
    </BasicAnchor>
  </div>
</template>

<script>
import { Icon } from "ant-design-vue";

const HeartSvg = {
  template: `
    <svg width="1em" height="1em" fill="currentColor" viewBox="0 0 1024 1024">
      <path d="M923 283.6c-13.4-31.1-32.6-58.9-56.9-82.8-24.3-23.8-52.5-42.4-84-55.5-32.5-13.5-66.9-20.3-102.4-20.3-49.3 0-97.4 13.5-139.2 39-10 6.1-19.5 12.8-28.5 20.1-9-7.3-18.5-14-28.5-20.1-41.8-25.5-89.9-39-139.2-39-35.5 0-69.9 6.8-102.4 20.3-31.4 13-59.7 31.7-84 55.5-24.4 23.9-43.5 51.7-56.9 82.8-13.9 32.3-21 66.6-21 101.9 0 33.3 6.8 68 20.3 103.3 11.3 29.5 27.5 60.1 48.2 91 32.8 48.9 77.9 99.9 133.9 151.6 92.8 85.7 184.7 144.9 188.6 147.3l23.7 15.2c10.5 6.7 24 6.7 34.5 0l23.7-15.2c3.9-2.5 95.7-61.6 188.6-147.3 56-51.7 101.1-102.7 133.9-151.6 20.7-30.9 37-61.5 48.2-91 13.5-35.3 20.3-70 20.3-103.3 0.1-35.3-7-69.6-20.9-101.9z" />
    </svg>
  `,
};
const PandaSvg = {
  template: `
    <svg viewBox="0 0 1024 1024" width="1em" height="1em" fill="currentColor">
      <path d="M99.096 315.634s-82.58-64.032-82.58-132.13c0-66.064 33.032-165.162 148.646-148.646 83.37 11.91 99.096 165.162 99.096 165.162l-165.162 115.614zM924.906 315.634s82.58-64.032 82.58-132.13c0-66.064-33.032-165.162-148.646-148.646-83.37 11.91-99.096 165.162-99.096 165.162l165.162 115.614z" fill="#6B676E" p-id="1143" />
      <path d="M1024 561.548c0 264.526-229.23 429.42-512.002 429.42S0 826.076 0 561.548 283.96 66.064 512.002 66.064 1024 297.022 1024 561.548z" fill="#FFEBD2" p-id="1144" />
      <path d="M330.324 842.126c0 82.096 81.34 148.646 181.678 148.646s181.678-66.55 181.678-148.646H330.324z" fill="#E9D7C3" p-id="1145" />
      <path d="M644.13 611.098C594.582 528.516 561.55 512 512.002 512c-49.548 0-82.58 16.516-132.13 99.096-42.488 70.814-78.73 211.264-49.548 247.742 66.064 82.58 165.162 33.032 181.678 33.032 16.516 0 115.614 49.548 181.678-33.032 29.18-36.476-7.064-176.93-49.55-247.74z" fill="#FFFFFF" p-id="1146" />
      <path d="M611.098 495.484c0-45.608 36.974-82.58 82.58-82.58 49.548 0 198.194 99.098 198.194 165.162s-79.934 144.904-148.646 99.096c-49.548-33.032-132.128-148.646-132.128-181.678zM412.904 495.484c0-45.608-36.974-82.58-82.58-82.58-49.548 0-198.194 99.098-198.194 165.162s79.934 144.904 148.646 99.096c49.548-33.032 132.128-148.646 132.128-181.678z" fill="#6B676E" p-id="1147" />
      <path d="M512.002 726.622c-30.06 0-115.614 5.668-115.614 33.032 0 49.638 105.484 85.24 115.614 82.58 10.128 2.66 115.614-32.944 115.614-82.58-0.002-27.366-85.556-33.032-115.614-33.032z" fill="#464655" p-id="1148" />
      <path d="M330.324 495.484m-33.032 0a33.032 33.032 0 1 0 66.064 0 33.032 33.032 0 1 0-66.064 0Z" fill="#464655" p-id="1149" />
      <path d="M693.678 495.484m-33.032 0a33.032 33.032 0 1 0 66.064 0 33.032 33.032 0 1 0-66.064 0Z" fill="#464655" p-id="1150" />
    </svg>
  `,
};
const HeartIcon = {
  template: `
    <a-icon :component="HeartSvg" />
  `,
  data() {
    return {
      HeartSvg,
    };
  },
};
const PandaIcon = {
  template: `
    <a-icon :component="PandaSvg" />
  `,
  data() {
    return {
      PandaSvg,
    };
  },
};
const IconFont = Icon.createFromIconfontCN({
  scriptUrl: "//at.alicdn.com/t/font_8d5l8fzk5b87iudi.js",
});

export default {
  data() {
    return {
      AntDesignVue: {
        fontSize: 30,
        color: "#111",
        spin: false,
        theme: "filled",
        type: "home",
        twoToneColor: "#ccc",
        rotate: 0,
      },
      ElementUI: {
        class: "el-icon-edit",
        fontSize: 30,
        color: "#111",
      },
      AtUI: {
        class: "icon icon-zoom-in",
        fontSize: 30,
        color: "#111",
      },
      ViewUI: {
        type: "ios-add-circle",
        size: 30,
        color: "#111",
      },
    };
  },
  components: {
    HeartIcon,
    PandaIcon,
    IconFont,
  },
  methods: {},
};
</script>