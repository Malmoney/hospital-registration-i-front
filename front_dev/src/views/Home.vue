<template>
  <div class="home">
    <div class="home_search"></div>
    <div class="home_head">
      <div class="home_head_title">诊前·诊中·诊后 全流程服务</div>
      <div class="home_head_content">
        <div
          v-for="(item, index) in 13"
          :key="index"
          class="home_head_content_item"
        >
          item
        </div>
      </div>
    </div>
    <div class="home_hospital_list">
      <HospitalList
        class="home_hospital_list_item"
        v-for="(item, index) in 4"
        :key="index"
      >
        <template v-slot:hospitalName>XXX医院</template>
        <template v-slot:hospitalInfo_info_level>三甲</template>
        <template v-slot:hospitalInfo_info_kind>综合医院</template>
        <template v-slot:hospitalInfo_info_distance>3.3km</template>
        <template v-slot:hospitalAddr
          >地址：山西省太原市小店区昌盛街51号银河公寓6号楼1单元602</template
        >
      </HospitalList>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HospitalList from "../components/hospital";

export default {
  name: "Home",
  components: {
    HospitalList
  }
};
</script>
<style>
.home {
  width: 100vw;
  min-height: 100vh;
  background-color: #f3f3f3;
}
.home_search {
  width: 100vw;
  height: 40px;
  background-color: yellow;
}
.home_head {
  width: 100vw;
  background-color: #ffffff;
}
.home_head_title {
  display: flex;
  align-items: center;
  height: 40px;
  width: 100%;
  font-size: 1.2em;
  text-align: left;
  padding-left: 10px;
  box-sizing: border-box;
  font-weight: 600;
}
.home_head_content {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
}
.home_head_content_item {
  width: 20%;
  height: 80px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.home_hospital_list {
  width: 100vw;
  margin-top: 20px;
}
</style>
