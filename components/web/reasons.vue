<template>
  <div>
    <section id="reasons" class="reasons">
      <b-container fluid>
        <b-row md="12" sm="12" align-v="center">
          <b-col md="4" class="reason1">
            <div class="content">
              <h3>Mengapa Memilih Prodi Sistem Informasi?</h3>
              <p>
                Beberapa alasan yang harus kita ketahui sebelum memilih program
                studi Sistem Informasi Institut Teknologi Telkom Purwokerto.
              </p>
              <b-button
                v-b-modal.modal-lg
                variant="primary"
                class="more-btn border-0"
                ><i class="fa fa-play"></i> Video Profil</b-button
              >

              <b-modal
                id="modal-lg"
                size="lg"
                centered
                title="Video Profil"
                hide-footer
              >
                <p class="my-4">
                  <iframe
                    src="https://www.youtube.com/embed/SZKQpEo4q9E?controls=0"
                    width="100%"
                    height="430"
                  />
                </p>
              </b-modal>
            </div>
          </b-col>
          <b-col md="8">
            <b-row md="12" sm="12">
              <b-col md="4" class="reason2">
                <div class="content-2">
                  <div class="icon-circle">
                    <img src="../../assets/img/icon-receipt.png" width="100%" />
                  </div>
                  <h4>Prospek Karir Lulusan yang Menjanjikan</h4>
                  <p>
                    Prospek karir lulusan Sistem Informasi sangat menjanjikan di
                    tengah semakin pesatnya perkembangan teknologi di era
                    seperti sekarang ini.
                  </p>
                </div>
              </b-col>
              <b-col md="4" class="reason2">
                <div class="content-2">
                  <div class="icon-circle">
                    <img src="../../assets/img/icon-cube.png" width="100%" />
                  </div>
                  <h4>Tertarget oleh Perusahaan dan Instansi Pemerintah</h4>
                  <p>
                    Lulusan Sistem Informasi menjadi lulusan yang sangat
                    dibutuhkan oleh perusahaan-perusahaan dan juga oleh instansi
                    pemerintahan.
                  </p>
                </div>
              </b-col>
              <b-col md="4" class="reason2">
                <div class="content-2">
                  <div class="icon-circle">
                    <img src="../../assets/img/icon-images.png" width="100%" />
                  </div>
                  <h4>Ilmu yang Didapatkan Sangat Aplikatif</h4>
                  <p>
                    Ilmu yang diajarkan saat perkuliahan sangat aplikatif
                    sehingga bisa memudahkan dalam beradaptasi di lingkungan
                    kerja nantinya.
                  </p>
                </div>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </b-container>
    </section>

    <section id="careers" class="careers">
      <b-container fluid>
        <div class="content">
          <h3>Prospek Karier</h3>
        </div>
        <b-row md="12" sm="12" align-v="center">
          <b-col md="3"
            ><div class="icon-box">
              <i class="fa fa-desktop" style="color: #ffbb2c"></i>
              <h3>IT Consultant</h3>
            </div></b-col
          >
          <b-col md="3"
            ><div class="icon-box">
              <i class="fa fa-code" style="color: #5578ff"></i>
              <h3>IS Developer</h3>
            </div></b-col
          >
          <b-col md="3"
            ><div class="icon-box">
              <i class="fa fa-database" style="color: #e80368"></i>
              <h3>Database Specialist</h3>
            </div></b-col
          >
          <b-col md="3"
            ><div class="icon-box">
              <i class="fa fa-user-graduate" style="color: #e361ff"></i>
              <h3>IS Academician</h3>
            </div></b-col
          >
        </b-row>
      </b-container>
    </section>
  </div>
</template>
