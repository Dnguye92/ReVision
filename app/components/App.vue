<template>
    <Page>
        <ActionBar title="ReVision" android:flat="true"/>
        <TabView android:tabBackgroundColor="#53ba82"
                 android:tabTextColor="#c4ffdf"
                 android:selectedTabTextColor="#ffffff"
                 androidSelectedTabHighlightColor="#ffffff">
            <TabViewItem title="Home" class="tab-1">
                <StackLayout>
                    <Image src="~/assets/images/splash.JPG" stretch="aspectFit"/>
                    <Label textWrap="true" text="Increasing the use of vision rehabilitation services by persons with visual impairment" @tap="onLinkTapped"/>
                </StackLayout>
            </TabViewItem>
            <TabViewItem title="Tab 2">
                <GridLayout columns="*" rows="*">
                    <Label class="message" text="Tab 2 Content" col="0" row="0"/>
                </GridLayout>
            </TabViewItem>
            <TabViewItem title="Tab 3">
                <GridLayout columns="*" rows="*">
                    <Label class="message" text="Tab 3 Content" col="0" row="0"/>
                </GridLayout>
            </TabViewItem>
            <TabViewItem title="Tab 4">
                <GridLayout columns="*" rows="*">
                    <Label class="message" text="Tab 2 Content" col="0" row="0"/>
                </GridLayout>
            </TabViewItem>
            <TabViewItem title="Tab 5">
                <GridLayout columns="*" rows="*">
                    <Label class="message" text="Tab 3 Content" col="0" row="0"/>
                </GridLayout>
            </TabViewItem>
            <TabViewItem title="Tab 6">
                <GridLayout columns="*" rows="*">
                    <Label class="message" text="Tab 3 Content" col="0" row="0"/>
                </GridLayout>
            </TabViewItem>
        </TabView>
    </Page>
</template>

<script >
  import Vue from 'nativescript-vue'
  import VueDevTools from 'nativescript-vue-devtools'
  const OpenUrl = require('nativescript-openurl');
  Vue.use(VueDevTools);

  export default {
    data() {
      return {
        msg: 'Hello World!'
      }
    },
    methods: {
      onLinkTapped() {
        OpenUrl('https://www.healthypeople.gov/2020/topics-objectives/topic/vision/objectives');
        console.log('Tapped!');
      }
    }
  }
</script>

<style scoped>
    ActionBar {
        background-color: #53ba82;
        color: #ffffff;
    }

    .message {
        vertical-align: center;
        text-align: center;
        font-size: 20;
        color: #333333;
    }

    .tab-1 Label {
      text-align: center;
    }
</style>
