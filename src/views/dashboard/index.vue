<template>
  <div class="dashboard-container">
    <div class="flex-row" style="justify-content:space-around">
      <!--  人员介绍  -->
      <div class="flex-1" style="width: 48%">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>作者：康真博</span>
            </div>
            <div v-for="o in 4" :key="o" class="text item">
              {{'列表内容 ' + o }}
            </div>
          </el-card>
      </div>
      <div class="flex-1" style="width: 48%">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>作者：安军</span>
            </div>
            <div v-for="o in 4" :key="o" class="text item">
              {{'列表内容 ' + o }}
            </div>
          </el-card>
      </div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'dashboard',
  computed: {
    ...mapGetters([
      'name',
      'roles'
    ])
  },
  data() {
    return {
      writerInfos: []
    }
  }
}
</script>

<style rel="stylesheet/scss" lang="scss" scoped>
.dashboard {
  &-container {
    margin: 30px;
  }
  &-text {
    font-size: 30px;
    line-height: 46px;
  }
}
</style>
