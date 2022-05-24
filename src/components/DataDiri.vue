<template>
    <div class="container">
        <div class="header">
            <div class="gambar">
                <img alt="Vue logo" class="logo" src="../assets/img/AhmadYunusWidodo.jpg" width="125" height="125" />
            </div>
            <div class="judul">
                <h1>AHMAD YUNUS WIDODO</h1>
                <span>programmer</span>
            </div>
        </div>
        <div class="content">
            <div class="content-left">
                <div class="card card-riwayad-pribadi">
                    <div class="card-judul">
                        <h2> &nbsp RIWAYAT PRIBADI</h2>
                    </div>
                    <div class="card-content" v-for="desc in descriptions">
                        <span>{{desc.desc}}
                        </span>
                    </div>
                </div>
                <div class="card card-skil">
                    <div class="card-judul">
                        <h2> &nbsp SKILL</h2>
                    </div>
                    <div class="card-content" v-for="skill in skills">
                        <span>-{{skill.name}}</span><br>
                    </div>
                </div>
                <div class="card card-kontak">
                    <div class="card-judul">
                        <h2> &nbsp KONTAK</h2>
                    </div>
                    <div class="card-content" v-for="contact in contacts">
                        <span>Nomor Hp/Wa : {{contact.nomor}}</span><br>
                        <span>eMail : {{contact.eMail}}</span><br>
                        <span>Alamat : {{contact.address}}</span><br>
                    </div>
                </div>
            </div>
            <div class="content-right">
                <div class="card pengalaman-Kerja">
                    <div class="card-judul">
                        <h2> &nbsp PENGALAMAN KERJA</h2>
                    </div>
                    <div class="card-content">
                        <h3>Intership Frontend Developer</h3>
                        <h4>jobhun.co.id | 2019 - 2019</h4>
                        <span>- Membangun tampilan website menggunakan  Bootstrap-vue.JS</span> <br>
                        <span>- Membangun website dengan Web Mobile First Besign</span> <br>
                        <span>- Berkolaborasi dengan Backend Developer </span> <br>
                        <span>- Mengambil data dari Backend via API JSON untuk ditampilkan</span> <br>
                        <span>- Bekerja bersama sesama developer dengan menggunakan GIT (github)   control version</span> <br>
                    </div>
                    
                    <div class="card-content">
                        <h3>Destop Developer</h3>
                        <h4>Software Gallery |  2020 - 2021</h4>
                        <span>- Membuat desain laporan  menggunakan Fastrport .fr3</span> <br>
                        <span>- Menampilkan data yang dibutuhkan oleh user  dengan Query SQL</span> <br>
                        <span>- Membuat tampilan aplikasi berbasis destop  </span> <br>
                    </div>
                    
                    <div class="card-content">
                        <h3>Front End Developer</h3>
                        <h4>Grand Devine Indonesia | 2021 - 2022</h4>
                        <span>- Mendesain tampilan website Enterprise menggunakan boostrap 5 dan Jquery.JS </span> <br>
                        <span>- Templating website Enterprise menggunakan boostrap 5 </span> <br>
                        <span>- Memperbaiki tampilan website yang kurang user friendly </span><br>
                        <span>- Membangun tampilan website dengan tampilan RWD (resposive web design)</span><br>
                        <span>- Membuat Map menggunakan Leaflet.JS dan API Mapbox </span>
                        <span>- Bekerja bersama sesama developer dengan menggunakan SVN (tortoise) control version</span>
                    </div>
                </div>
                <div class="card card-pendidikan">
                    <div class="card-judul">
                        <h2> &nbsp LATAR BELAKANG PENDIDIKAN</h2>
                    </div>
                    <div class="card-content" v-for="pendidikan in pendidikan">
                        <h3>{{pendidikan.name}}</h3>
                        <span>{{pendidikan.prodi}} | {{pendidikan.tahun-masuk}} - {{pendidikan.tahun-keluar}}</span><br>
                        <span>IPK : {{pendidikan.ipk}}</span><br>
                        <br> <br>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

  <script>
    import usersData from "../users.json";
    import pendidikanData from "../pendidikan.json";
    import skillsData from "../skills.json";
    import contactsData from "../contacts.json";
    import descriptionsData from "../descriptions.json";

    export default {
      data() {
        return {
          users: usersData,
          pendidikan: pendidikanData,
          skills: skillsData,
          contacts: contactsData,
          descriptions : descriptionsData
        };
      },
    };

    
    </script>
  
  <style scoped>
    .container 
    {
        width: 900px;
        margin: auto;
        border: solid 1px black;
        height: 990px;
        
    }
    .header{
        display: flex;
    }
    .gambar{
        width: 300px;
        display: flex;
        justify-content: center;

    }
    /* image radius  */
    img 
    {
        border-radius: 50%;
        width: 200px;
        height: 200px;
    }

    .judul {
        width: 600px;
        text-align: center;
        color: white;
        background-color: #373741;

    }
    h1 {
      margin-top: 40px;
      margin-left: 20px;
      font-weight: 5000px;
      font-size: 40px;  
    }
    
    .content
    {
        display: flex;
        flex-direction: row;
    }

    .content-left
    {
        width: 300px;
        display: flex;
        flex-direction: column;
    }

    /* global card */
    .card 
    {    
        margin-top: 20px;
    }

    .card-judul
    {
        text-align: left;
        color: white;
        background-color: #373741;
    }

    .card-content
    {
        margin-top: 10px;
        margin-left: 10px;
    }
    /* end global card  */

    /* selector only class this */
    .card, .card-riwayad-pribadi, .card-content:only-child
    {
        /* color: red; */
        
    }

    .card-skil {
        margin-bottom: 60px !important;
    }

    .content-right
    {
        width: 590px;
        height: 10px;
        margin-left: 10px;
        display: flex;
        flex-direction: column;
    }

    </style>
    