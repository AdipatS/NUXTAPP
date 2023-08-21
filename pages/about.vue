<template>
    <div class="text-center mt-2">
        <img :src="picture" :width="size" :height="auto"> 
        <p class="mt-2">ชื่อ :{{ getFullname() }}</p>
        <p>นามสกุล :{{ lastname }}</p>
        <p>อายุ : {{ age }}</p>
        <p>ที่อยู่ : <span v-html="address"></span></p>
        <p v-if="hobby.length ===0">ไม่มีงานอดิเรก</p>
        <div v-else>
        <p>งานอดิเรก :</p>
            <ul>
                <li v-for="item in hobby">{{ item }}</li>
            </ul>
        </div>
        <p>ข้อมูลพื้นฐาน : </p>
            <ul>
                <li v-for="(value,key) in general" :key="key">{{ key }}:{{ value }}</li>
            </ul>
                <button @click="showData">คลิกเพื่อดูข้อมูล</button>
                <button @click="increment(10)">เพิ่มค่า</button>
                <button @click="decrement(3)">ลดค่า</button>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                firstname: "Adipat",
                lastname: "Sompong",
                age: 18,
                address: "<i>Chonburi</i>",
                picture:"http://www.106planet.com/66309010019/img/FB_IMG_1688624333586.jpg",
                size:250,
                hobby : ["ทำไร่","ทำสวน","นอน","นอน","นอน"],
                general : {เพศ:"ชาย",น้ำหนัก:95,ส่วนสูง:174,โรคประจำตัว:false}
            }
        },
        methods:{
            getFullname(){
                return `${this.firstname} ${this.lastname}`
            },
            showData(){
                alert(this.firstname)
            },
            increment(value){
                this.age += value
            },
            decrement(value){
                this.age -= value
            },
            setNickName(event){
                this.nickname=event.target.value
            },
            submitForm(e){
                e.preventDefault();
                alert('บันทึกข้อมูลเรียบร้อย')
            }
        }
    }
    
</script>