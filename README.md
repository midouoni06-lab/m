<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="utf-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>الأكاديمية الفيلسوف الصغير - رئيسية</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<style>
  :root{--nav:#023e8a;--accent:#0077b6;--light:#a0c4ff}
  body{margin:0;font-family:"Cairo",sans-serif;direction:rtl;background:linear-gradient(180deg,var(--light),#ffffff);min-height:100vh;overflow-x:hidden}
  nav{background:var(--nav);color:#fff;padding:12px 18px;display:flex;align-items:center;justify-content:space-between;position:fixed;top:0;left:0;right:0;z-index:50;box-shadow:0 2px 10px rgba(0,0,0,.15)}
  nav .brand{display:flex;align-items:center;gap:12px}
  nav img{width:48px;height:48px;border-radius:10px;animation:bounce 2s infinite}
  nav h2{margin:0;font-size:18px}
  nav .actions{display:flex;gap:12px;align-items:center}
  nav button{background:transparent;border:1px solid rgba(255,255,255,.18);color:#fff;padding:8px 12px;border-radius:8px;cursor:pointer}
  .container{padding:120px 20px 40px;max-width:1100px;margin:0 auto}
  .hero{text-align:center;color:var(--nav)}
  .hero h1{font-size:34px;margin:6px 0}
  .hero p{color:#03045e;font-size:17px;margin:6px 0 18px}
  .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(250px,1fr));gap:22px;margin-top:30px}
  .card{background:#fff;border-radius:16px;padding:18px;box-shadow:0 8px 20px rgba(2,62,138,.08);text-align:center}
  .card img{width:96px;height:96px;object-fit:contain;margin-bottom:12px}
  .card h3{color:var(--nav);margin:8px 0}
  .card p{color:#6d82a2;font-size:14px}
  .card button{margin-top:12px;background:linear-gradient(90deg,var(--accent),#00b4d8);border:none;padding:10px 14px;border-radius:10px;color:#fff;cursor:pointer}
  footer{background:var(--nav);color:#fff;text-align:center;padding:14px;margin-top:30px;border-radius:10px}
  /* modal */
  .modal{position:fixed;inset:0;display:none;place-items:center;background:rgba(2,6,23,.45);z-index:100}
  .modal.show{display:grid}
  .panel{background:#fff;padding:18px;border-radius:12px;min-width:320px;max-width:420px;box-shadow:0 8px 30px rgba(2,62,138,.2)}
  .panel h3{margin:0 0 8px;color:var(--nav)}
  .field{margin:8px 0}
  .field input,.field select{width:100%;padding:10px;border-radius:8px;border:1px solid #d1d5db;font-size:14px}
  .row{display:flex;gap:8px}
  .small{font-size:13px;color:#6b7280;margin-top:6px}
  .hidden{display:none}
  @keyframes bounce{0%,20%,50%,80%,100%{transform:translateY(0)}40%{transform:translateY(-8px)}60%{transform:translateY(-4px)}}
  .top-right-badge{position:fixed;top:74px;left:18px;background:#fff;padding:10px;border-radius:10px;box-shadow:0 8px 20px rgba(2,62,138,.12);z-index:40}
  /* responsive tweaks */
  @media (max-width:520px){nav h2{display:none}.panel{width:92vw}}
</style>
</head>
<body>

<nav>
  <div class="brand">
<!-- #endregion -->    <div>
      <h2>الأكاديمية الفيلسوف الصغير</h2>
      <div style="font-size:12px;opacity:.9">منصة تعليمية للتلاميذ</div>
    </div>
  </div>

  <div class="actions">
    <div id="userArea" style="display:flex;align-items:center;gap:10px">
      <button id="openLoginBtn">تسجيل / دخول</button>
    </div>
    <div id="memberArea" style="display:none;align-items:center;gap:8px">
      <div id="welcomeText" style="color:#fff;font-size:14px"></div>
      <button id="openDashboardBtn" style="background:#ffd60a;color:#000;border:none;padding:8px 10px;border-radius:8px;cursor:pointer">لوحة</button>
      <button id="logoutBtn">خروج</button>
    </div>
  </div>
</nav>

<div class="top-right-badge hidden" id="roleBadge"></div>

<div class="container">
  <section class="hero">
    <h1>مرحبًا بكم في الأكاديمية الفيلسوف الصغير 🎓</h1>
    <p>تعلم - اكتشف - استمتع. منصة تفاعلية للدروس، التمارين، ورفع المحتوى بواسطة الأساتذة.</p>
  </section>

  <section class="grid" id="stagesGrid">
    <div class="card">
      <img src="https://cdn-icons-png.flaticon.com/512/2729/2729077.png" alt="">
      <h3>المرحلة الثانية</h3>
      <p>دروس وأنشطة ممتعة تناسب المرحلة الثانية.</p>
      <button onclick="openStage('2')">ابدأ التعلم</button>
    </div>
    <div class="card">
      <img src="https://cdn-icons-png.flaticon.com/512/4326/4326930.png" alt="">
      <h3>المرحلة الثالثة</h3>
      <p>تمارين وفيديوهات تفاعلية للمرحلة الثالثة.</p>
      <button onclick="openStage('3')">ابدأ التعلم</button>
    </div>
    <div class="card">
      <img src="https://cdn-icons-png.flaticon.com/512/4147/4147345.png" alt="">
      <h3>ألعاب تعليمية</h3>
      <p>أنشطة ترفيهية وتعلمية لتعزيز المهارات.</p>
      <button onclick="alert('قريبًا!')">جرب الآن</button>
    </div>

    <div class="card">
      <img src="https://cdn-icons-png.flaticon.com/512/1250/1250615.png" alt="">
      <h3>المكتبة</h3>
      <p>مقاطع فيديو، ملفات، وكتب تعليمية.</p>
      <button onclick="alert('قريبًا!')">افتح المكتبة</button>
    </div>
  </section>

  <footer style="margin-top:40px;border-radius:12px">
    © 2025 الأكاديمية الفيلسوف الصغير – جميع الحقوق محفوظة.
  </footer>
</div>

<!-- Modal تسجيل/تسجيل دخول -->
<div class="modal" id="authModal">
  <div class="panel">
    <h3 id="modalTitle">تسجيل / تسجيل دخول</h3>

    <div id="authForms">
      <!-- tabs -->
      <div class="row" style="margin-bottom:8px">
        <button id="tabLogin" style="flex:1">تسجيل دخول</button>
        <button id="tabRegister" style="flex:1">تسجيل حساب</button>
      </div>

      <!-- تسجيل دخول -->
      <div id="loginForm">
        <div class="field"><input id="loginEmail" type="email" placeholder="البريد الإلكتروني"></div>
        <div class="field"><input id="loginPassword" type="password" placeholder="كلمة المرور"></div>
        <div class="field"><button id="loginBtn" style="width:100%">دخول</button></div>
        <div class="small">هل نسيت كلمة المرور؟ <a href="#" id="resetPassLink">إعادة تعيين</a></div>
      </div>

      <!-- تسجيل -->
      <div id="registerForm" class="hidden">
        <div class="field"><input id="regName" type="text" placeholder="الاسم"></div>
        <div class="field"><input id="regEmail" type="email" placeholder="البريد الإلكتروني"></div>
        <div class="field"><input id="regPassword" type="password" placeholder="كلمة المرور"></div>
        <div class="field">
          <select id="regRole">
            <option value="">اختر الدور</option>
            <option value="child">طفل</option>
            <option value="teacher">أستاذ</option>
          </select>
        </div>
        <div class="field"><button id="registerBtn" style="width:100%">إنشاء حساب</button></div>
        <div class="small">بإنشاء حساب توافق على شروط الاستخدام.</div>
      </div>
    </div>

    <div style="text-align:left;margin-top:12px">
      <button id="closeModal" style="background:transparent;border:none;color:#6b7280;cursor:pointer">إغلاق</button>
    </div>
  </div>
</div>

<!-- لوحة الأستاذ (صفحة بسيطة موقتة داخل نفس الملف لعرض الفكرة) -->
<div class="modal" id="teacherPanel">
  <div class="panel">
    <h3>لوحة الأستاذ</h3>
    <div id="teacherContent">
      <div class="field"><input id="lessonTitle" placeholder="عنوان الدرس"></div>
      <div class="field"><select id="lessonStage"><option value="2">المرحلة الثانية</option><option value="3">المرحلة الثالثة</option></select></div>
      <div class="field"><input type="file" id="lessonFile"></div>
      <div class="field"><button id="uploadLessonBtn">رفع الدرس</button></div>
      <div id="uploadStatus" class="small"></div>
    </div>
    <div style="text-align:left;margin-top:12px">
      <button id="closeTeacher" style="background:transparent;border:none;color:#6b7280;cursor:pointer">إغلاق</button>
    </div>
  </div>
</div>

<!-- Firebase SDK -->
<script type="module">
  // --------------- ضع تهيئة Firebase هنا ----------------
  import { initializeApp } from "https://www.gstatic.com/firebasejs/9.23.0/firebase-app.js";
  import { getAuth, onAuthStateChanged, createUserWithEmailAndPassword, signInWithEmailAndPassword, signOut, sendPasswordResetEmail } from "https://www.gstatic.com/firebasejs/9.23.0/firebase-auth.js";
  import { getFirestore, doc, setDoc, getDoc, collection, addDoc, query, where, getDocs } from "https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore.js";
  import { getStorage, ref as sRef, uploadBytes, getDownloadURL } from "https://www.gstatic.com/firebasejs/9.23.0/firebase-storage.js";

  const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT.firebaseapp.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
  };
  const app = initializeApp(firebaseConfig);
  const auth = getAuth(app);
  const db = getFirestore(app);
  const storage = getStorage(app);
  // ----------------------------------------------------

  // عناصر DOM
  const authModal = document.getElementById('authModal');
  const openLoginBtn = document.getElementById('openLoginBtn');
  const closeModal = document.getElementById('closeModal');
  const tabLogin = document.getElementById('tabLogin');
  const tabRegister = document.getElementById('tabRegister');
  const loginForm = document.getElementById('loginForm');
  const registerForm = document.getElementById('registerForm');

  const loginEmail = document.getElementById('loginEmail');
  const loginPassword = document.getElementById('loginPassword');
  const loginBtn = document.getElementById('loginBtn');

  const regName = document.getElementById('regName');
  const regEmail = document.getElementById('regEmail');
  const regPassword = document.getElementById('regPassword');
  const regRole = document.getElementById('regRole');
  const registerBtn = document.getElementById('registerBtn');

  const memberArea = document.getElementById('memberArea');
  const userArea = document.getElementById('userArea');
  const welcomeText = document.getElementById('welcomeText');
  const logoutBtn = document.getElementById('logoutBtn');
  const openDashboardBtn = document.getElementById('openDashboardBtn');
  const roleBadge = document.getElementById('roleBadge');

  const teacherPanel = document.getElementById('teacherPanel');
  const closeTeacher = document.getElementById('closeTeacher');
  const uploadLessonBtn = document.getElementById('uploadLessonBtn');
  const lessonFile = document.getElementById('lessonFile');
  const lessonTitle = document.getElementById('lessonTitle');
  const lessonStage = document.getElementById('lessonStage');
  const uploadStatus = document.getElementById('uploadStatus');

  // فتح وغلق المودال
  openLoginBtn.addEventListener('click',()=>{authModal.classList.add('show')});
  closeModal.addEventListener('click',()=>{authModal.classList.remove('show')});
  tabLogin.addEventListener('click',()=>{loginForm.classList.remove('hidden');registerForm.classList.add('hidden')});
  tabRegister.addEventListener('click',()=>{registerForm.classList.remove('hidden');loginForm.classList.add('hidden')});

  // تسجيل مستخدم جديد وحفظ الدور في Firestore
  registerBtn.addEventListener('click', async ()=>{
    const name = regName.value.trim(); const email = regEmail.value.trim(); const pass = regPassword.value; const role = regRole.value;
    if(!name||!email||!pass||!role){alert('الرجاء ملء جميع الحقول واختيار الدور');return;}
    try{
      const userCred = await createUserWithEmailAndPassword(auth,email,pass);
      const uid = userCred.user.uid;
      // حفظ ملف المستخدم في Firestore
      await setDoc(doc(db,'users',uid),{name, email, role, createdAt: new Date()});
      alert('تم إنشاء الحساب بنجاح');
      authModal.classList.remove('show');
    }catch(err){
      alert('خطأ: '+err.message);
    }
  });

  // تسجيل دخول
  loginBtn.addEventListener('click', async ()=>{
    const email = loginEmail.value.trim(); const pass = loginPassword.value;
    if(!email||!pass){alert('الرجاء ملء الحقول');return;}
    try{
      await signInWithEmailAndPassword(auth,email,pass);
      authModal.classList.remove('show');
    }catch(err){alert('فشل الدخول: '+err.message)}
  });

  // إعادة تعيين كلمة المرور
  document.getElementById('resetPassLink').addEventListener('click',async (e)=>{
    e.preventDefault();
    const email = loginEmail.value.trim();
    if(!email){alert('ضع بريدك في حقل البريد لإرسال رابط الاستعادة');return;}
    try{ await sendPasswordResetEmail(auth,email); alert('تم إرسال رابط إعادة التعيين إلى بريدك'); }
    catch(err){alert('خطأ: '+err.message)}
  });

  // مراقبة حالة الدخول
  onAuthStateChanged(auth, async (user)=>{
    if(user){
      // جلب بيانات المستخدم (role, name)
      const uDoc = await getDoc(doc(db,'users',user.uid));
      const data = uDoc.exists()? uDoc.data() : {name:'مستخدم', role:'child'};
      welcomeText.textContent = أهلاً ${data.name};
      userArea.style.display = 'none';
      memberArea.style.display = 'flex';
      roleBadge.classList.remove('hidden');
      roleBadge.textContent = data.role === 'teacher' ? 'أستاذ' : 'طالب';
      // إذا كان أستاذ فعّال، أظهر زر اللوحة
      if(data.role === 'teacher'){ openDashboardBtn.style.display = 'inline-block'; } else { openDashboardBtn.style.display = 'none'; }
    } else {
      userArea.style.display = 'flex';
      memberArea.style.display = 'none';
      roleBadge.classList.add('hidden');
    }
  });

  // خروج
  logoutBtn.addEventListener('click', async ()=>{ await signOut(auth); alert('تم تسجيل الخروج'); });

  // فتح لوحة الأستاذ (مودال داخل نفس الصفحة كمثال)
  openDashboardBtn.addEventListener('click',()=>{ teacherPanel.classList.add('show'); });
  closeTeacher.addEventListener('click',()=>{ teacherPanel.classList.remove('show'); });

  // رفع درس - مثال: يخزن ملف في Storage ويوضح رابط في Firestore collection "lessons"
  uploadLessonBtn.addEventListener('click', async ()=>{
    const user = auth.currentUser;
    if(!user){ alert('يجب تسجيل الدخول'); return; }
    // فقط الأساتذة يمكنهم رفع الدروس
    const uDoc = await getDoc(doc(db,'users',user.uid));
    if(!uDoc.exists() || uDoc.data().role !== 'teacher'){ alert('هذه الخاصية متاحة للأساتذة فقط'); return; }

    const title = lessonTitle.value.trim();
    const stage = lessonStage.value;
    const file = lessonFile.files[0];
    if(!title||!file){ alert('ضع عنوانًا واختر ملفًا'); return; }

    try{
      uploadStatus.textContent = 'جارٍ رفع الملف...';
      const fileRef = sRef(storage,`lessons/${user.uid}/${Date.now()}_${file.name}`);
      const snapshot = await uploadBytes(fileRef, file);
      const url = await getDownloadURL(snapshot.ref);
      // سجل الدرس في Firestore
      await addDoc(collection(db,'lessons'),{
        title, stage, url, owner: user.uid, createdAt: new Date()
      });
      uploadStatus.textContent = 'تم الرفع بنجاح ✅';
      lessonTitle.value = ''; lessonFile.value = '';
    }catch(err){
      uploadStatus.textContent = 'خطأ: '+err.message;
    }
  });


  // دالة فتح مرحلة (مثال؛ يمكن تعديلها لفتح صفحة خاصة)
  function openStage(stage){
    alert('فتح محتوى المرحلة '+stage+' — (يمكن ربط هذه الوظيفة بصفحات دروس)'); 
  }

  // تعيين بعض عناصر افتراضية
  window.openStage = openStage;
</script>
</body>
</html>
