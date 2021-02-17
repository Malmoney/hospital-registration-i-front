<template>
  <div class="hospital">
    <div class="hospital_mian">
      <div class="hospital_mian_coverimg">
        <slot name="hospital_mian_coverimg"></slot>
      </div>
      <div class="hospital_mian_right">
        <div class="hospitalName">
          <slot name="hospitalName"></slot>
        </div>
        <div class="hospitalInfo">
          <div class="hospitalInfo_info_level">
            <slot name="hospitalInfo_info_level"></slot>
            <div class="hospitalInfo_info_kind">
              <slot name="hospitalInfo_info_kind"></slot>
            </div>
          </div>
          <div class="hospitalInfo_info_distance">
            <slot name="hospitalInfo_info_distance"></slot>
          </div>
        </div>
        <div class="hospitalAddr">
          <slot name="hospitalAddr"></slot>
        </div>
      </div>
    </div>
    <div class="hospital_foot"></div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.hospital {
  width: 95%;
  height: 150px;
  background-color: #ffffff;
  margin: auto;
  margin-bottom: 10px;
  border-radius: 8px;
}
.hospital_mian {
  width: 100%;
  height: 130px;
  padding: 10px;
  box-sizing: border-box;
  display: flex;
  justify-content: space-between;
}
.hospital_mian_coverimg {
  height: 100%;
  width: 140px;
  background-color: red;
}
.hospital_mian_right {
  height: 100%;
  width: calc(100% - 150px);
}
.hospital_mian_right div {
  height: calc(110px / 3);
  line-height: calc(110px / 3);
}
.hospitalName {
  text-align: left;
  font-size: 1.1em;
}
.hospitalInfo {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.hospitalInfo_info_level {
  font-size: 0.9em;
  display: flex;
  color: #e97b24;
}
.hospitalInfo_info_kind {
  font-size: 0.8em;
  margin-left: 5px;
  color: #6b7aac;
  width: 60px;
}
.hospitalAddr {
  text-align: left;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  font-size: 0.9em;
}
.hospital_foot {
  width: 100%;
  height: 20px;
}
</style>
