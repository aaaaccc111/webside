<template>
  <main class="bg-white min-h-screen text-slate-900 font-sans">
    <button
      @click="switchLanguage"
      class="fixed top-6 right-6 px-4 py-2 rounded-xl bg-white text-slate-900 border border-red-500 z-50 hover:bg-red-50 transition"
    >
      {{ locale === 'zh' ? 'EN' : '中文' }}
    </button>

    <section class="relative min-h-screen overflow-hidden flex items-center justify-center">
      <div class="absolute w-[700px] h-[700px] bg-cyan-50/60 rounded-full blur-[120px] top-[-200px] left-[-200px]"></div>
      <div class="absolute w-[500px] h-[500px] bg-purple-50/60 rounded-full blur-[120px] bottom-[-100px] right-[-100px]"></div>

      <div class="z-10 text-center px-6">
        <p class="text-cyan-600 tracking-[0.3em] uppercase mb-4 text-sm font-bold">
          Full Stack / Software Engineer<br>{{ t('Herderword') }}

        </p>
        <h1 class="text-5xl md:text-5xl font-black leading-tight text-slate-900">
          Hunter Yin
        </h1>

        <div class="flex flex-wrap gap-4 justify-center mt-12 max-w-5xl mx-auto">
          <button @click="scrollTo('about-me')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            {{ t('about') }}
          </button>
          <button @click="scrollTo('education')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            {{ t('education') }}
          </button>
          <button @click="scrollTo('experience')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            {{ t('experience') }}
          </button>
          <button @click="scrollTo('skills')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            {{ t('skills') }}
          </button>
          <button @click="scrollTo('projects')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            {{ t('projects') }}
          </button>
        </div>
      </div>
    </section>

    <section id="about-me" class="py-24 bg-slate-50/50" data-aos="fade-up">
    <div class="max-w-4xl mx-auto px-6">
        <h3 class="text-3xl font-bold mb-8 text-center">{{ t('about') }}</h3>

        <div
        @click="toggleModal"
        class="bg-white p-10 rounded-3xl shadow-sm leading-loose text-slate-600 italic cursor-pointer hover:shadow-md hover:border-cyan-200 border border-transparent transition-all group"
        >
        {{ t('about1') }}
        <p class="text-xs text-cyan-500 mt-4 text-right not-italic opacity-50 group-hover:opacity-100">{{ t('about2') }} →</p>
        </div>
    </div>

    <Teleport to="body">
    <Transition name="fade">
        <div v-if="isModalOpen" class="fixed inset-0 z-[100] flex items-center justify-center p-6">
        <div class="absolute inset-0 bg-slate-900/60 backdrop-blur-sm" @click="toggleModal"></div>

        <div class="bg-white w-full max-w-2xl max-h-[85vh] rounded-3xl shadow-2xl z-10 overflow-hidden flex flex-col">
            <div class="p-6 border-b border-slate-100 flex justify-between items-center bg-white sticky top-0 z-20">
            <button @click="toggleModal" class="text-slate-400 hover:text-slate-600 text-3xl transition-colors">&times;</button>
            </div>

            <div class="p-8 overflow-y-auto text-slate-600 leading-relaxed">
            <div class="space-y-6">
                <p>
                {{ t('about3') }} <span class="text-cyan-600 font-bold">Hunter</span>{{ t('about4') }}
                </p>
                <p>
                {{ t('about5') }}
                </p>

                <p>
                {{ t('about6') }}
                </p>
                <hr class="border-slate-100" />
                <div>
                <ul class="space-y-2 pl-4 border-l-2 border-slate-100">
                    <li>• {{ t('about7') }}</li>
                    <li>• {{ t('about8') }}</li>
                </ul>
                </div>

                <!-- <p>
                {{ t('about9') }}
                </p> -->

                <p>
                {{ t('about10') }}
                </p>
                <hr class="border-slate-100" />
                <div>
                <ul class="space-y-2 pl-4 border-l-2 border-slate-100">
                    <!-- <li>• {{ t('about11') }}</li> -->
                    <li>• {{ t('about12') }}</li>
                    <!-- <li>• {{ t('about13') }}</li> -->
                </ul>
                </div>

                <!-- <p>
                {{ t('about14') }}
                </p> -->

                <!-- <p>
                {{ t('about15') }}
                </p> -->
                <p>
                {{ t('about16') }}
                </p>

                <p class="font-bold text-slate-800">{{ t('about17') }}</p>
            </div>
            </div>

        </div>
        </div>
    </Transition>
    </Teleport>
    </section>

    <section id="education" class="py-24 bg-white" data-aos="fade-right">
      <div class="max-w-4xl mx-auto px-6">
        <h3 class="text-3xl font-bold mb-12 text-center">{{ t('education') }}</h3>
        <div class="flex flex-col md:flex-row justify-between items-center p-8 bg-slate-50 rounded-3xl border border-slate-100">
          <div class="text-center md:text-left">
            <h4 class="text-xl font-bold">{{ t('education1') }}</h4>
            <p class="text-cyan-600 font-medium">{{ t('education2') }}</p>
          </div>
          <div class="mt-4 md:mt-0 text-slate-500 italic">
            2022/9 - 2026/6
          </div>
        </div>
      </div>
    </section>

    <section id="experience" class="py-24 bg-slate-50/50">
      <div class="max-w-4xl mx-auto px-6">
        <h3 class="text-3xl font-bold mb-16 border-l-4 border-cyan-500 pl-4" data-aos="fade-right"">{{ t('experience') }}</h3>
        <div class="space-y-16">
          <div class="relative pl-8 border-l border-slate-200" data-aos="fade-up">
            <div class="absolute w-4 h-4 bg-cyan-500 rounded-full -left-[8.5px] top-1"></div>
            <h4 class="text-xl font-bold">{{ t('experience1') }}</h4>
            <h4 class="text-xl font-bold">{{ t('experience2') }}</h4>
            <h4 class="text-xl font-bold">{{ t('experience3') }}</h4>
            <p class="text-slate-500 text-sm mb-4">2022/10 - NOW </p>
            <ul class="list-disc list-inside space-y-2 text-slate-600 leading-relaxed">
              <li>{{t('experience4')}}</li>
              <li>{{t('experience5')}}</li>
              <li>{{t('experience6')}}</li>
              <li>{{t('experience7')}}</li>
              <li>{{t('experience8')}}</li>
              <li>{{t('experience9')}}</li>
              <li>{{t('experience10')}}</li>
              <li>{{t('experience11')}}</li>
            </ul>
          </div>
          <div class="relative pl-8 border-l border-slate-200" data-aos="fade-up" data-aos-delay="200">
            <div class="absolute w-4 h-4 bg-slate-300 rounded-full -left-[8.5px] top-1"></div>
            <h4 class="text-xl font-bold">{{ t('experience12') }}</h4>
            <h4 class="text-xl font-bold">{{ t('experience13') }}</h4>
            <h4 class="text-xl font-bold">{{ t('experience14') }}</h4>
            <p class="text-slate-500 text-sm mb-4">2020/8 - 2022/9</p>
            <ul class="list-disc list-inside space-y-2 text-slate-600 leading-relaxed">
              <li>{{t('experience15')}}</li>
              <li>{{t('experience16')}}</li>
              <li>{{t('experience17')}}</li>
              <li>{{t('experience18')}}</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="skills" class="py-24 bg-white">
      <div class="max-w-6xl mx-auto px-6">
        <h3 class="text-3xl font-bold text-center mb-16" data-aos="fade-right"">{{ t('skills') }}</h3>
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
          <div class="bg-white p-8 rounded-3xl shadow-sm border border-slate-100 hover:shadow-md transition" data-aos="flip-left" data-aos-delay="300">
            <h4 class="text-xl font-bold text-cyan-600 mb-6">Software Engineering</h4>
            <ul class="space-y-3 text-slate-600">
              <li>Python 、Java 、C 、C++ 、 C#</li>
              <li>Eclipse IDE</li>
              <li>Java</li>
              <li>Visual Studio Code</li>
              <li>Visual Studio</li>

            </ul>
          </div>
          <div class="bg-white p-8 rounded-3xl shadow-sm border border-slate-100 hover:shadow-md transition" data-aos="flip-left" data-aos-delay="500">
            <h4 class="text-xl font-bold text-purple-600 mb-6">Web</h4>
            <ul class="space-y-3 text-slate-600">
              <li>JavaScript、CSS、HTML</li>
              <li>Vue.js、Node.js</li>
              <li>Python Flask</li>
              <li>RESTful API</li>
            </ul>
          </div>
          <div class="bg-white p-8 rounded-3xl shadow-sm border border-slate-100 hover:shadow-md transition" data-aos="flip-left" data-aos-delay="500">
            <h4 class="text-xl font-bold text-purple-600 mb-6">Database</h4>
            <ul class="space-y-3 text-slate-600">
              <li>Oracle</li>
              <li>MSSQL</li>
              <li>MYSQL</li>
              <li>SQLite</li>
            </ul>
          </div>
          <div class="bg-white p-8 rounded-3xl shadow-sm border border-slate-100 hover:shadow-md transition" data-aos="flip-left" data-aos-delay="700">
            <h4 class="text-xl font-bold text-emerald-600 mb-6">Management</h4>
            <ul class="space-y-3 text-slate-600">
              <li>Microsoft SharePoint</li>
              <li>Microsoft365</li>
              <li>Microsoft Active Directory</li>
              <li>Microsoft Azure</li>
              <li>Microsoft Exchange</li>
              <li>NSA 、 PLM 、 GitHub</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="projects" class="py-24 bg-slate-50/50">
    <div class="max-w-4xl mx-auto px-6">
        <h3 class="text-3xl font-bold mb-12 text-center" data-aos="fade-up">{{ t('projects') }}</h3>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-start">

        <div class="group bg-white p-8 rounded-3xl shadow-sm border border-slate-100 hover:shadow-xl transition-all duration-500 cursor-pointer overflow-hidden"
            data-aos="flip-left" data-aos-delay="300">
            <h5 class="font-bold text-lg mb-2 text-cyan-600">軟體紀錄系統</h5>
            <p class="text-slate-600 text-sm">
            透過 WMI 監控軟體使用效率，透明化授權分配，成功為公司節省逾 30% 軟體採購支出。
            </p>

            <div class="max-h-0 opacity-0 group-hover:max-h-60 group-hover:opacity-100 group-hover:mt-6 transition-all duration-500 ease-in-out">
            <div class="pt-4 border-t border-slate-100">
                <ul class="text-xs text-slate-500 space-y-2 mb-4">
                <li>• 紀錄軟體使用狀態（結合JSON）抓取特定軟體資訊</li>
                <li>• 以作業系統背景程式運行，降低使用者干擾</li>
                <li>• 採 C/S 架構，支援 Server 端同步與離線作業模式</li>
                <li>• 成功部署於 20 台以上端點，為公司節省逾 30% 軟體採購支出</li>
                <li>• Python WMI 架構應用、Javascript、HTML、CSS、chart.js、Python Flask框架</li>
                </ul>
                <a href="#" class="inline-flex items-center text-xs font-bold text-cyan-600 hover:text-cyan-700">
                Github Repo
                <svg class="w-3 h-3 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
                </a>
            </div>
            </div>
        </div>

        <div class="group bg-white p-8 rounded-3xl shadow-sm border border-slate-100 hover:shadow-xl transition-all duration-500 cursor-pointer overflow-hidden"
            data-aos="flip-left" data-aos-delay="500">
            <h5 class="font-bold text-lg mb-2 text-cyan-600">專案管理系統</h5>
            <p class="text-slate-600 text-sm">
            配合研發專案成本，帶入員工研發工時，確保專案工時分配透明化，達成企業內部的成本規律化與節流目標。
            </p>

            <div class="max-h-0 opacity-0 group-hover:max-h-60 group-hover:opacity-100 group-hover:mt-6 transition-all duration-500 ease-in-out">
            <div class="pt-4 border-t border-slate-100">
                <ul class="text-xs text-slate-500 space-y-2 mb-4">
                <li>• 自動抓取使用者對應的專案代碼，填寫日工時。</li>
                <li>• 每月結算開發金費給予財務，由財務核算成本</li>
                <li>• 結合內部 Mail Server 提醒功能</li>
                <li>• Vue.js、Node.js、Oracle</li>
                </ul>
            </div>
            </div>
        </div>

        <div class="group bg-white p-8 rounded-3xl shadow-sm border border-slate-100 hover:shadow-xl transition-all duration-500 cursor-pointer overflow-hidden"
            data-aos="flip-left" data-aos-delay="300">
            <h5 class="font-bold text-lg mb-2 text-cyan-600">遠端工作機管理工具</h5>
            <p class="text-slate-600 text-sm">
            基於 Python 開發的輕量化自動化連線工具，優化企業內部共用遠端電腦的配置效率。
            </p>

            <div class="max-h-0 opacity-0 group-hover:max-h-60 group-hover:opacity-100 group-hover:mt-6 transition-all duration-500 ease-in-out">
            <div class="pt-4 border-t border-slate-100">
                <ul class="text-xs text-slate-500 space-y-2 mb-4">
                <li>• 透過 API 預先檢查伺服器狀態，避免多人重複連線。</li>
                <li>• 自動新增與移除 Windows 憑證，使用者無需手動輸入帳密。</li>
                <li>• 提供 GUI 介面，每 5 秒自動更新工作機連線狀態。</li>
                <li>• Python</li>
                </ul>
                <a href="#" class="inline-flex items-center text-xs font-bold text-cyan-600 hover:text-cyan-700">
                Github Repo
                <svg class="w-3 h-3 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
                </a>
            </div>
            </div>
        </div>

        <div class="group bg-white p-8 rounded-3xl shadow-sm border border-slate-100 hover:shadow-xl transition-all duration-500 cursor-pointer overflow-hidden"
            data-aos="flip-left" data-aos-delay="300">
            <h5 class="font-bold text-lg mb-2 text-cyan-600">用於資安的 SharePoint 檔案下載通知</h5>
            <p class="text-slate-600 text-sm">
            一套自動化系統，主動追蹤下載紀錄並透過組織架構進行發信告知，強化企業資安攔截能力。
            </p>

            <div class="max-h-0 opacity-0 group-hover:max-h-60 group-hover:opacity-100 group-hover:mt-6 transition-all duration-500 ease-in-out">
            <div class="pt-4 border-t border-slate-100">
                <ul class="text-xs text-slate-500 space-y-2 mb-4">
                <li>• 串接 Office 365 Management Activity API，抓取 FileDownloaded 操作事件。</li>
                <li>• 自動發送信給下載者，建立資安意識。。</li>
                <li>• 向 Office API 請求活動內容 URI，並分段下載詳細記錄 JSON。</li>
                <li>• Python</li>
                </ul>
                <a href="#" class="inline-flex items-center text-xs font-bold text-cyan-600 hover:text-cyan-700">
                Github Repo
                <svg class="w-3 h-3 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
                </a>
            </div>
            </div>
        </div>

        </div>
    </div>
    </section>

    <footer class="py-12 text-center text-slate-400 text-sm border-t border-slate-100 bg-white">
      © 2026 Hunter
    </footer>
  </main>
</template>


<script setup>
import { onMounted, ref } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';
import { useI18n } from 'vue-i18n';

const isModalOpen = ref(false);
const { t, locale } = useI18n();
const switchLanguage = () => {
  locale.value = locale.value === 'zh' ? 'en' : 'zh'
}

onMounted(() => {
  AOS.init({
    duration: 1000,
    once: false,
    mirror: true,
    offset: 100,
  });
});

const toggleModal = () => {
  isModalOpen.value = !isModalOpen.value;
  document.body.style.overflow = isModalOpen.value ? 'hidden' : 'auto';
};

const scrollTo = (id) => {
  const element = document.getElementById(id);
  if (element) {
    element.scrollIntoView({
      behavior: 'smooth',
      block: 'start'
    });
  }
};

</script>
