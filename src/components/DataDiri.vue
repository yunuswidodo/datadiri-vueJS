<template>
    <div class="container">
        <div class="header" v-for="header in headers">
            <div class="gambar">
                <img alt="Vue logo" class="logo" src="../assets/img/AhmadYunusWidodo.jpg" width="125" height="125" />
            </div>
            <div class="judul">
                <h1>{{header.name}}</h1>
                <span>{{header.profesi}}</span>
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
                <div class="card pengalaman-Kerja" >
                    <div class="card-judul">
                        <h2> &nbsp PENGALAMAN KERJA</h2>
                    </div>
                    <div class="card-content"  v-for="exp in exps">
                        <h3>{{exp.postion}}</h3>
                        <h4>{{exp.comapanyname}} | {{exp.yearwork}}</h4>
                            <div class="job-desc" v-for="jobdes in exp.job"> 
                                <span>{{jobdes.jobdetail}}</span> <br>
                            </div>
                    </div>
                </div>
                <div class="card card-pendidikan">
                    <div class="card-judul">
                        <h2> &nbsp LATAR BELAKANG PENDIDIKAN</h2>
                    </div>
                    <div class="card-content" v-for="pendidikan in pendidikan">
                        <h3>{{pendidikan.name}}</h3>
                        <span>{{pendidikan.prodi}} | {{pendidikan.tahunmasuk}} - {{pendidikan.tahunkeluar}}</span><br>
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
    import experiencesData from "../experiences.json"
    import headersData from "../header.json"

    export default {
      data() {
        return {
          users: usersData,
          pendidikan: pendidikanData,
          skills: skillsData,
          contacts: contactsData,
          descriptions : descriptionsData,
          exps: experiencesData,
          headers: headersData
        };
      },
    };

    console.log("#detail-job");
    
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
    