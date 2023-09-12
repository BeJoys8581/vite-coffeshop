<script setup>
import { ref } from 'vue';

const coffeeShops = ref([
  {
    id: 1,
    name: 'ใบพลู',
    description:'ร้านใบพลูเป็นร้านอาหารที่อยู่ในซอยที่ไม่มีร้านอาหารอื่นอยู่ ทำให้นั่งกินอาหาร 🍽 ฟังเพลงกันแบบชิลล์ ๆ 🎼 โดยไม่มีดนตรีจากร้านอื่นมารบกวน บรรยากาศภายในร้านก็ตกแต่งสบาย น่านั่งด้วยแสงสีวอร์มไลต์  แถมยังมีดนตรีสดตั้งแต่เวลา 20:30 - 22:30 น.' ,
    address: 'ซอย ชีกุน 2 ตำบลท่าวาสุกรี อำเภอ พระนครศรีอยุธยา จังหวัดพระนครศรีอยุธยา 13000' ,
    imageSrc:"https://www.thai2night.com/upload/shop/photo_cover/master/shop_shop_photo_cover_9480_1661584413.jpg",
  },
  {
    id: 2,
    name: 'The Story',
    description:' The Story รอให้คุณมาสัมผัสบรรยากาศใหม่ๆ สบายๆ ชิลๆ ทางร้านมีบริการทั้งโซนห้องแอร์และโซน outdoor และบรรยากาศ outdoor ก็มองเห็นโบราณสถาน บอกเลยว่าคุณจะได้อิ่มหนำกับ อาหารอร่อยๆ 🍽 และเพลงเพราะๆแนวยุค 90s อย่างเต็มที่ จากนักดนตรีผู้มีสามารถล้นเหลือ 🎼' ,
    address: '9/28-31 ประตูชัย เทศบาลนครพระนครศรีอยุธยา 13000' ,
    imageSrc:"https://www.thai2night.com/upload/shop/photo_cover/master/121491828_166303148482812_7661239556833659210_o.jpg",
  },
  {
    id: 3,
    name: 'Coffee House',
    description:'Coffee House เป็น ร้านอาหารใหญ่ใจกลางเมืองอยุธยา ให้อาหารมื้อค่ำของคุณเป็นมื้อพิเศษกับบรรยากาศสุดชิล ฟังดนตรีสดเพราะๆ อาหารอร่อย ถ่ายรูปสวย ร้านกว้างโปร่งโล่งนั่งสบาย รับจัดเลี้ยงพิเศษต่างๆ บอกเลยว่ามาครบจบที่นี่!' ,
    address: 'ถนน นเรศวร เทศบาลนครพระนครศรีอยุธยา 13000 ' ,
    imageSrc:"https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRyArdw4jfTDwUARbf4rHi-b0aRLI7HyLBddAqZ4K_R9raVsFaJVAPUvRy82XQ_mj1rXuk&usqp=CAU",
  },
  {
    id: 4,
    name: 'ค.แข็ง',
    description:'มาซอยนี้ต้อง ค.แข็ง ซอยฝรั่ง ซอยธกส แฮงค์เอ้าท์ที่ใหม่อยุธยา' ,
    address: 'ซอย ถนน นเรศวร ตำบลหัวรอ อำเภอ พระนครศรีอยุธยา จังหวัดพระนครศรีอยุธยา 13000 ประเทศไทย เทศบาลนครพระนครศรีอยุธยา 13000' ,
    imageSrc:"https://i.pinimg.com/750x/6f/60/c9/6f60c93afdd132138ffa097b8e146b69.jpg",
  },
  {
    id: 5,
    name: 'The Soi',
    description:'แฮงเอาท์ชิลๆในบรรยากาศสบายๆ' ,
    address: '14/9 ตำบล หัวรอ อำเภอ พระนครศรีอยุธยา จังหวัดพระนครศรีอยุธยา 13000 เทศบาลนครพระนครศรีอยุธยา 13000' ,
    imageSrc:"https://scontent.fcnx3-1.fna.fbcdn.net/v/t39.30808-6/277579126_3285447608404983_1717424494833679722_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=5614bc&_nc_eui2=AeH9c5ViULEnJe7Y7b54lq1Z0smo9T6__knSyaj1Pr_-SXimPFG59_Qz0DhVeZNLHwFRwOr3c-dE_-RSGSj1CaDg&_nc_ohc=Ok_HuWM4zhgAX-fxRwR&_nc_ht=scontent.fcnx3-1.fna&oh=00_AfArrZ_g0AVURGVJ_lNjtOVErvqIS_242M-LtKSLxx2M8Q&oe=6500E1C8",
  },
  {
    id: 6,
    name: 'Camping BAR Ayutthaya',
    description:'ร้านลับๆกลางทุ่งนามาๆ  โปรชั้นเพียบ Camping bar' ,
    address: 'เทศบาลนครพระนครศรีอยุธยา 13000' ,
    imageSrc:"https://scontent.fcnx3-1.fna.fbcdn.net/v/t39.30808-6/366741231_304581012102718_2666544644703561045_n.jpg?stp=cp6_dst-jpg&_nc_cat=109&ccb=1-7&_nc_sid=5614bc&_nc_eui2=AeEPBOj-4t_SlZ0KtdpxaX6yUlL0Uv8-H_RSUvRS_z4f9OnCkWE0bz_qs6r3C_vucc0HcOVJEexWVbBK-gln2ACB&_nc_ohc=SIegASjsk2kAX_UwtlF&_nc_ht=scontent.fcnx3-1.fna&oh=00_AfBfHAf5RkkpaJ2YOar9SjI5C3sFa9XYWzSUq11l4Mv0wg&oe=6501A664",
  },
]);

// const reservation = ref(null);

//const Table = (shop) => {
 // const name = prompt('ชื่อ:');
 // const phone = prompt('เบอร์โทร:');
 // const date = prompt('วันที่:');
 // const time = prompt('เวลา:');
 // const tableCount = prompt('จำนวนโต๊ะ:');

  //reservation.value = {
   // shopId : shop.id,
   // name,
   // phone,
   // date,
   // time,
   // tableCount,
 // };
//};  

//const getShopName = (shopId) => {
 // const shop = coffeeShops.value.find(shop => shop.id === shopId);
 // return shop ? shop.name : '';
//};

const Details = ref({
    name: "",
    tel: "",
    date: "",
    time: "",
    tables: ""
  });

  const bookingList = ref([
  ]);

  function booking(shop, Details) {

  const bookingData = {
    coffeeShopName: shop.name,
    name: Details.name,
    tel: Details.tel,
    date: Details.date,
    time: Details.time,
    tables: Details.tables,
  };

  bookingList.value.push(bookingData);

  Details.name = '';
  Details.tel = '';
  Details.date = '';
  Details.time = '';
  Details.tables = '';

  alert("ทำการจองโต๊ะสำเร็จแล้ว ! เช็คข้อมูลได้ข้างล่าง ");
}

</script>


<template>
  <h1 style="color: white;">จองโต๊ะร้านกาแฟ (หรือป่าวน้าา)</h1><br>
  <div class="container-input" style="background-color: #242627;">
    <h4 style="color: rgb(255, 255, 255); font-weight: bold;">- ใส่ข้อมูลก่อนจองโต๊ะ -</h4><br>
    <div class="bom">
          <div class="text-input">
            ชื่อ  &nbsp; <input type="text" v-model="Details.name" required> 
          </div>
          <div class="text-input">
            เบอร์โทร &nbsp; <input type="tel" v-model="Details.tel" required >  
          </div>
          <div class="text-input">  
            วัน/เดือน/ปี &nbsp; <input type="date" v-model="Details.date" required>
          </div>
          <div class="text-input">
            เวลา &nbsp; <input type="time" v-model="Details.time" required>
          </div>
          <div class="text-input">
            โต๊ะ &nbsp; <input type="number" v-model="Details.tables" required > 
          </div>
    </div><br>
    <h4 style="color: rgb(245, 0, 0); font-weight: bold;">* กรุณาเช็คข้อมูลให้ครบถ้วนก่อนจองโต๊ะ *</h4>
  </div><br>

  <div class="row">
    <div class="col-md-4" v-for="shop in coffeeShops" :key="shop.id">
      <div class="card">
        <img :src="shop.imageSrc" class="card-img-top"><br>
        <div class="card-body">
          <div class="card">
            <h3 class="card-title">ร้าน {{ shop.name }}</h3><br>
            <h6 class="card-title" style="font-size: small;">ที่อยู่ <br> {{ shop.address }}</h6><br>
            <p class="card-text">รายละเอียดร้าน <br> {{ shop.description }}</p>
          </div>
        </div>
        <button @click="booking(shop,Details)">จองโต๊ะ !</button>
      </div>
    </div>
  </div>


  <!-- <div v-if="reservation">
  <h2>รายละเอียดการจอง</h2>
  <div class="reservation-details">
    <span>ชื่อร้าน: {{ getShopName(reservation.shopId) }}</span>
    <span>ชื่อลูกค้า: {{ reservation.name }}</span>
    <span>เบอร์โทร: {{ reservation.phone }}</span>
    <span>วันที่: {{ reservation.date }}</span>
    <span>เวลา: {{ reservation.time }}</span>
    <span>จำนวนโต๊ะ: {{ reservation.tableCount }}</span>
  </div>
</div> -->

<div class="reservation-details" v-if="bookingList.length > 0">
  <table class="table table-dark table-striped">                                                             
    <thead>
      <tr>
        <th scope="col">ชื่อร้าน</th>
        <th scope="col">ชื่อผู้จอง</th>
        <th scope="col">เบอร์โทร</th>
        <th scope="col">วัน/เดือน/ปี</th>
        <th scope="col">เวลา</th>
        <th scope="col">จำนวนโต๊ะ</th>
      </tr>
    </thead>
  <tbody>
    <tr v-for="(booking, index) in bookingList" :key="index">
  <td>{{ booking.coffeeShopName }}</td>
  <td>{{ booking.name }}</td>
  <td>{{ booking.tel }}</td>
  <td>{{ booking.date }}</td>
  <td>{{ booking.time }}</td>
  <td>{{ booking.tables }}</td>
</tr>
  </tbody>
</table>
</div>
 <br>


</template>





