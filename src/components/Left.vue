<template>
	<mu-col width="20" tablet="20" desktop="20" class="row-left ">
        <mu-list class="list-menu">
          <mu-list-item title="仪表盘" class="menu-active">
            <mu-icon value="av_timer" slot="left">
            </mu-icon>
          </mu-list-item>
          <mu-list-item title="文章" :toggleNested="true">
            <mu-icon value="art_track" slot="left">
            </mu-icon>
            <mu-list-item title="写文章" slot="nested">
              <mu-icon value="border_color" slot="left">
              </mu-icon>
            </mu-list-item>
            <mu-list-item title="分类" slot="nested">
              <mu-icon value="folder" slot="left">
              </mu-icon>
            </mu-list-item>
          </mu-list-item>
          <mu-list-item title="多媒体">
            <mu-icon value="image" slot="left">
            </mu-icon>
          </mu-list-item>
          <mu-list-item title="页面">
            <mu-icon value="pages" slot="left">
            </mu-icon>
          </mu-list-item>
          <mu-list-item title="评论">
            <mu-icon value="comment" slot="left">
            </mu-icon>
          </mu-list-item>
          <mu-list-item title="外观">
            <mu-icon value="format_paint" slot="left">
            </mu-icon>
          </mu-list-item>
          <mu-list-item title="插件">
            <mu-icon value="settings_input_hdmi" slot="left">
            </mu-icon>
          </mu-list-item>
          <mu-list-item title="用户">
            <mu-icon value="people" slot="left">
            </mu-icon>
          </mu-list-item>
          <mu-list-item title="工具">
            <mu-icon value="build" slot="left">
            </mu-icon>
          </mu-list-item>
          <mu-list-item title="设置">
            <mu-icon value="settings" slot="left">
            </mu-icon>
          </mu-list-item>
        </mu-list>
      </mu-col>
</template>

<script>
</script>

<style>
</style>