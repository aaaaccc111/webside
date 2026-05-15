<template>
  <main class="bg-white min-h-screen text-slate-900 font-sans">
    <div id="google_translate_element"></div>

    <section class="relative min-h-screen overflow-hidden flex items-center justify-center">
      <div class="absolute w-[700px] h-[700px] bg-cyan-50/60 rounded-full blur-[120px] top-[-200px] left-[-200px]"></div>
      <div class="absolute w-[500px] h-[500px] bg-purple-50/60 rounded-full blur-[120px] bottom-[-100px] right-[-100px]"></div>

      <div class="z-10 text-center px-6">
        <p class="text-cyan-600 tracking-[0.3em] uppercase mb-4 text-sm font-bold">
          Full Stack / Software Engineer<br>以解決實際業務問題為目標，將技術落實為可運行的系統方案

        </p>

        <h1 class="text-5xl md:text-5xl font-black leading-tight text-slate-900">
          Hunter Yin
        </h1>

        <div class="flex flex-wrap gap-4 justify-center mt-12 max-w-5xl mx-auto">
          <button @click="scrollTo('about-me')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            關於我
          </button>
          <button @click="scrollTo('education')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            學歷
          </button>
          <button @click="scrollTo('experience')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            工作經歷
          </button>
          <button @click="scrollTo('skills')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            技術能力
          </button>
          <button @click="scrollTo('projects')" class="px-6 py-3 rounded-2xl border border-slate-200 text-slate-600 hover:border-cyan-500 hover:text-cyan-600 transition duration-300 font-semibold hover:scale-105 bg-white/50 backdrop-blur-md">
            專案成就
          </button>
        </div>
      </div>
    </section>

    <section id="about-me" class="py-24 bg-slate-50/50" data-aos="fade-up">
    <div class="max-w-4xl mx-auto px-6">
        <h3 class="text-3xl font-bold mb-8 text-center">關於我</h3>

        <div
        @click="toggleModal"
        class="bg-white p-10 rounded-3xl shadow-sm leading-loose text-slate-600 italic cursor-pointer hover:shadow-md hover:border-cyan-200 border border-transparent transition-all group"
        >
        「擁有6年橫跨軟硬體領域經驗，近4年專注於應用程式及全端開發，並能獨立主導企業內部系統從需求分析、架構設計至部署的「 0 到 1 」完整過程 。」
        <p class="text-xs text-cyan-500 mt-4 text-right not-italic opacity-50 group-hover:opacity-100">查看完整自傳 →</p>
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
                嗨，我是 <span class="text-cyan-600 font-bold">Hunter</span>，畢業於國立勤益科技大學資訊工程系。
                </p>
                <p>
                擁有超過 6 年跨領域實務資歷，職涯由硬體研發起步，現專注於全端系統開發與軟體自動化的應用。我具備獨立主導「0 到 1」系統開發的完整實力，能準確將商業需求轉化為高效能的數位化系統。
                </p>

                <p>
                在先前擔任兩年的硬體工程師中
                </p>
                <hr class="border-slate-100" />
                <div>
                <ul class="space-y-2 pl-4 border-l-2 border-slate-100">
                    <li>• 負責驗票機電路板的檢修與電路的設計規劃，並參與到了完整的驗票機開發流程、程式驗證、程式測試、軟體自動化程式檢修以及客戶端的售後服務。</li>
                    <li>• 取得無線通訊技術、點對點的串列通訊協定、網際網路協議等相關專業知識與技能。</li>
                </ul>
                </div>

                <p>
                也因為接觸到了這種精密設備，培養了我從底層架構分析問題的邏輯思維。之後便帶著這些深厚的硬體實務經驗，重返校園完成四年的資訊工程學業，將思維從硬體架構擴展至軟體架構。
                </p>

                <p>
                就讀大學四年期間，我在現職公司擔任助理工程師，從早期的電腦檢修到現在的程式設計，並獨立主導多項數位化系統專案：
                </p>
                <hr class="border-slate-100" />
                <div>
                <ul class="space-y-2 pl-4 border-l-2 border-slate-100">
                    <li>• 結合大學專題的軟體使用紀錄系統，可用於紀錄軟體使用狀態、計算軟體使用成本、透明化軟體使用財務經費、開源節流。</li>
                    <li>• 接連完成專案工時系統、 PriceBook 系統，有效達成研發部門研發成本透明化、大幅降低人工計算成本、工時支出比及財務健全、零件成本透明化、歷年零件支出比、毛利率等。</li>
                    <li>• 開發具有資安防護的鎖網卡工具、可以提升開發單位工作效率的管理工具、分散使用者的遠端連線工具。</li>

                </ul>
                </div>

                <p>
                也因此獲得單位主管的認同與期盼，並於在職期間持續學習相關專業知識及開發工具，並持續提供最優的解決方案。
                </p>

                <p>
                在學期間，除了充分學習本業相關專業知識，也於課外時間做小型專案（Side Project）、包括社會議題探討、數據分析等，並閱讀自己感興趣的書本，提升自己的價值。
                </p>
                <p>
                在這六年的職涯，我同時具備「硬體結構」與「軟體開發」的雙重背景，能跨技術進行高效的溝通，更能從系統整體的穩定性與可落地性進行思考。也於課外時間積極精進語文能力與程式語言等相關專業知識，期待能將過往跨領域的整合經驗帶入貴團隊，為企業提供最好的解決方案。
                </p>

                <p class="font-bold text-slate-800">謝謝。</p>
            </div>
            </div>

        </div>
        </div>
    </Transition>
    </Teleport>
    </section>

    <section id="education" class="py-24 bg-white" data-aos="fade-right">
      <div class="max-w-4xl mx-auto px-6">
        <h3 class="text-3xl font-bold mb-12 text-center">教育程度</h3>
        <div class="flex flex-col md:flex-row justify-between items-center p-8 bg-slate-50 rounded-3xl border border-slate-100">
          <div class="text-center md:text-left">
            <h4 class="text-xl font-bold">國立勤益科技大學</h4>
            <p class="text-cyan-600 font-medium">資訊工程系 學士</p>
          </div>
          <div class="mt-4 md:mt-0 text-slate-500 italic">
            2022年9月 - 2026年6月
          </div>
        </div>
      </div>
    </section>

    <section id="experience" class="py-24 bg-slate-50/50">
      <div class="max-w-4xl mx-auto px-6">
        <h3 class="text-3xl font-bold mb-16 border-l-4 border-cyan-500 pl-4" data-aos="fade-right"">工作經歷</h3>
        <div class="space-y-16">
          <div class="relative pl-8 border-l border-slate-200" data-aos="fade-up">
            <div class="absolute w-4 h-4 bg-cyan-500 rounded-full -left-[8.5px] top-1"></div>
            <h4 class="text-xl font-bold">助理工程師 | ＯＯ股份有限公司 |  其他電子零組件相關業</h4>
            <p class="text-slate-500 text-sm mb-4">2022年10月 - 至今 | 3年8個月</p>
            <ul class="list-disc list-inside space-y-2 text-slate-600 leading-relaxed">
              <li>主導三套內部系統開發，從需求分析、系統架構、程式撰寫、部屬完整的 SDLC 流程</li>
              <li>使用 Python 開發監控系統，並完成C/S架構，成功部署於 20 台以上端點，透過 WMI 監控軟體狀態並即時回傳，透明化軟體使用效率，為公司節省30%以上軟體支出。</li>
              <li>具備 Vue 3 實戰經驗，從專案工時系統至 PriceBook 介面，整合資料庫並設計 RESTful API，成功取代傳統紙本作業及成本規格化，顯著提升專案透明度並達成節流目標 。</li>
              <li>具備 Python、Java 與 Node 後端開發經驗 ，能獨立完成 RESTful API 設計、資料庫管理與前端串接，具備從無到有建構完整系統的即戰力 。</li>
              <li>針對同仁需求開發三項 Python 桌面軟體，優化使用單位專案開發流程，有效加速專案進度 。</li>
              <li>管理 Oracle、MSSQL、MySQL 等資料庫及 AD / SharePoint / M365 權限，確保企業核心資料的安全與存取控制。</li>
              <li>維護及管理產品開發生命週期 (Product Lifecycle Management，PLM) ，使用部門有更高效率的開發空間。</li>
              <li>維護全公司 100 台以上資訊設備，負責系統備份、硬體維修、異常檢查，確保公司營運環境穩定並符合資安政策。</li>
            </ul>
          </div>
          <div class="relative pl-8 border-l border-slate-200" data-aos="fade-up" data-aos-delay="200">
            <div class="absolute w-4 h-4 bg-slate-300 rounded-full -left-[8.5px] top-1"></div>
            <h4 class="text-xl font-bold text-slate-700">工程師 | ＯＯＯ科技股份有限公司 | 消費性電子產品製造業</h4>
            <p class="text-slate-500 text-sm mb-4">2020年8月 - 2022年9月 | 2年1個月</p>
            <ul class="list-disc list-inside space-y-2 text-slate-600 leading-relaxed">
              <li>針對業主需求進行驗票機系統程式開發與功能驗證，確保產品符合標案規格。</li>
              <li>參與驗票機初期設計與硬體規劃，優化機體內部配置以提升耐用度。</li>
              <li>執行精密電路板檢查與系統檢修，針對硬體失效進行根本原因分析，維持產品穩定性。</li>
              <li>結合NFC / RFID 、 RS-232 / RS-485、 TCP/IP 等相關通訊技術。</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section id="skills" class="py-24 bg-white">
      <div class="max-w-6xl mx-auto px-6">
        <h3 class="text-3xl font-bold text-center mb-16" data-aos="fade-right"">技術能力</h3>
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
        <h3 class="text-3xl font-bold mb-12 text-center" data-aos="fade-up">專案成就</h3>
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

const isModalOpen = ref(false);

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
