<template>
  <div class="form-config-container">
    <el-form label-position="top">
      <el-form-item :label="fm.config.form.labelPosition.title">
        <el-radio-group v-model="data.labelPosition">
          <el-radio-button label="left">{{fm.config.form.labelPosition.left}}</el-radio-button>
          <el-radio-button label="right">{{fm.config.form.labelPosition.right}}</el-radio-button>
          <el-radio-button label="top">{{fm.config.form.labelPosition.top}}</el-radio-button>
        </el-radio-group>
      </el-form-item>

      <el-form-item :label="fm.config.form.labelWidth">
        <el-input-number v-model="data.labelWidth" :min="0" :max="200" :step="10"></el-input-number>
      </el-form-item>

      <el-form-item :label="fm.config.form.size">
        <el-radio-group v-model="data.size">
          <el-radio-button label="medium">medium</el-radio-button>
          <el-radio-button label="small">small</el-radio-button>
          <el-radio-button label="mini">mini</el-radio-button>
        </el-radio-group>
      </el-form-item>

      <el-form-item :label="fm.config.form.cssEnhance">
        <el-input v-model="data.cssEnhance" type="textarea"></el-input>
      </el-form-item>

      <el-form-item :label="fm.config.form.jsEnhance">
        <el-input v-model="data.jsEnhance" type="textarea"></el-input>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  props: ['data'],
  data () {
    return {
    }
  }
}
</script>
