# [НоваСтрой.html](https://github.com/user-attachments/files/28183552/default.html)
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>НоваСтрой | Инженерное проектирование</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', 'Segoe UI', 'Roboto', 'Helvetica Neue', sans-serif;
            background: #f4f7fc;
            color: #1e2a32;
            line-height: 1.5;
            scroll-behavior: smooth;
        }

        /* Шрифт для заголовков — Book Antiqua */
        h1, h2, h3, h4, .logo h1, .module-header h2, .hero-welcome h2, .card-content h3, .lesson-block h3 {
            font-family: 'Book Antiqua', 'Georgia', 'Times New Roman', serif;
            font-weight: 600;
        }

        @import url('https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap');

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 28px;
        }

        /* Шапка строгая */
        .header {
            background: #0a1c24;
            color: #eef3f7;
            padding: 1rem 0;
            box-shadow: 0 4px 12px rgba(0,0,0,0.08);
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 1px solid #2c4755;
        }
        .header .container {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 16px;
        }
        /* Логотип + название в одной строке */
        .logo {
            display: flex;
            align-items: center;
            gap: 14px;
            flex-wrap: wrap;
        }
        .logo-icon {
    		width: 72px;
    		height: 72px;
    		background: white;
    		border-radius: 18px;
    		display: flex;
    		align-items: center;
    		justify-content: center;
    		overflow: hidden;
    		box-shadow: 0 4px 12px rgba(0,0,0,0.2);
    		transition: transform 0.2s;
    		padding: 4px;
		}
	.logo-icon img {
    		width: 100%;
    		height: 100%;
    		object-fit: contain;
		}
	.logo-icon:hover {
    		transform: scale(1.03);
		}
        .logo-text h1 {
            font-size: 2.5rem; /* Увеличен размер названия */
            font-weight: 700;
            letter-spacing: -0.3px;
            color: white;
            margin-bottom: 4px;
        }
        .logo-text p {
            font-size: 0.75rem;
            opacity: 0.8;
            margin-top: 2px;
            font-weight: 400;
            letter-spacing: 0.3px;
        }
        .nav-links {
            display: flex;
            gap: 1.4rem;
            flex-wrap: wrap;
            align-items: center;
        }
        .nav-links a {
            color: #cfdfe8;
            text-decoration: none;
            font-weight: 500;
            font-size: 0.9rem;
            transition: 0.2s;
            border-bottom: 2px solid transparent;
            padding-bottom: 4px;
        }
        .nav-links a:hover {
            color: white;
            border-bottom-color: #9aaeb9;
        }
        /* Кнопки личного кабинета */
        .auth-buttons {
            display: flex;
            gap: 12px;
            margin-left: 10px;
        }
        .btn-outline {
            background: transparent;
            border: 1px solid #8aaebd;
            color: #e0f0f7;
            padding: 6px 16px;
            border-radius: 40px;
            font-weight: 500;
            cursor: pointer;
            transition: 0.2s;
            font-size: 0.85rem;
        }
        .btn-outline:hover {
            background: rgba(255,255,255,0.1);
            border-color: white;
        }
        .btn-primary-auth {
            background: #e8b86b;
            border: none;
            color: #1f2f36;
            padding: 6px 18px;
            border-radius: 40px;
            font-weight: 600;
            cursor: pointer;
            transition: 0.2s;
            font-size: 0.85rem;
        }
        .btn-primary-auth:hover {
            background: #f3c97e;
        }
        .user-greeting {
            font-size: 0.85rem;
            color: #d9e9f0;
            display: flex;
            align-items: center;
            gap: 12px;
        }
        .logout-btn {
            background: none;
            border: 1px solid #a0b8c4;
            padding: 4px 12px;
            border-radius: 30px;
            color: #ffd966;
            cursor: pointer;
        }

        #app-root {
            min-height: 70vh;
            padding: 2rem 0 3rem;
        }

        /* сетка модулей */
        .modules-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }
        .module-card {
            background: white;
            border-radius: 28px;
            overflow: hidden;
            box-shadow: 0 20px 30px -12px rgba(0,0,0,0.1);
            transition: transform 0.2s, box-shadow 0.2s;
            cursor: pointer;
            display: flex;
            flex-direction: column;
            height: 100%;
        }
        .module-card:hover {
            transform: translateY(-6px);
            box-shadow: 0 28px 36px -14px rgba(0,0,0,0.2);
        }
        /* Цветные иконки как было (без grayscale) */
        .card-img {
            height: 160px;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            font-weight: 500;
            color: white;
        }
	.module-icon{
    		width:1024px;
    		height:160px;
    		object-fit:contain;
	}
        .card-content {
            padding: 1.6rem;
            flex-grow: 1;
        }
        .card-content h3 {
            font-size: 1.7rem;
            margin-bottom: 0.75rem;
            color: #0f3b4c;
        }
        .card-content p {
            color: #2c5368;
            margin-bottom: 1.2rem;
        }
        .tag {
            display: inline-block;
            background: #eef2f5;
            padding: 0.25rem 0.9rem;
            border-radius: 40px;
            font-size: 0.8rem;
            font-weight: 500;
            color: #1f6e8c;
        }
        .btn-module {
            margin-top: 1rem;
            background: #1f6e8c;
            border: none;
            color: white;
            padding: 0.6rem 1.2rem;
            border-radius: 40px;
            font-weight: 600;
            cursor: pointer;
            transition: 0.2s;
            width: fit-content;
        }
        .btn-module:hover {
            background: #0a4b63;
        }

        /* страницы модулей */
        .module-page {
            background: white;
            border-radius: 32px;
            padding: 2rem 2rem 2.5rem;
            box-shadow: 0 10px 25px -8px rgba(0,0,0,0.06);
        }
        .module-header {
            margin-bottom: 2rem;
            border-left: 6px solid #f5a623;
            padding-left: 1.2rem;
        }
        .module-header h2 {
            font-size: 2.2rem;
            color: #0b2b3b;
        }
        .module-header p {
            color: #3a6b7e;
            font-size: 1.1rem;
        }
        .learning-section {
            display: flex;
            flex-direction: column;
            gap: 2rem;
        }
        .lesson-block {
            background: #f9fafc;
            border-radius: 24px;
            padding: 1.5rem;
            border: 1px solid #e2edf2;
        }
        .lesson-block h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: #1c5d78;
        }
        .lesson-block ul, .lesson-block p {
            margin-top: 0.5rem;
            margin-left: 1.2rem;
            color: #2c3e44;
        }
        .video-placeholder {
            background: #eef3f7;
            border-radius: 20px;
            padding: 1rem;
            margin-top: 1rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            flex-wrap: wrap;
            border: 1px solid #cbdae2;
        }
        .teacher-list {
            background: #f1f5f8;
            padding: 0.8rem 1.2rem;
            border-radius: 28px;
            margin-top: 1rem;
            font-size: 0.9rem;
            border-left: 3px solid #6f8f9c;
        }
        .back-home-btn {
            background: #e2e8f0;
            border: none;
            padding: 0.6rem 1.4rem;
            border-radius: 40px;
            font-weight: 600;
            margin-top: 2.5rem;
            cursor: pointer;
            transition: 0.2s;
            color: #1f3e48;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }
        footer {
            background: #0f1f27;
            color: #bcd1db;
            text-align: center;
            padding: 1.6rem;
            font-size: 0.85rem;
            margin-top: 2rem;
            border-top: 1px solid #294552;
        }
        .authors-line {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1rem;
            margin-top: 0.6rem;
            font-size: 0.8rem;
        }
        .hero-welcome {
            background: linear-gradient(135deg, #eef5f9 0%, #deeaf1 100%);
            border-radius: 32px;
            padding: 2rem;
            margin-bottom: 2rem;
            text-align: center;
        }
        .hero-welcome h2 {
            font-size: 2rem;
            color: #074154;
        }
        .project-authors {
            background: white;
            border-radius: 28px;
            padding: 1.2rem 1.8rem;
            margin-top: 2rem;
            text-align: center;
            border: 1px solid #dce4ea;
        }
        .author-names {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.5rem;
            font-weight: 500;
            color: #1f4c5e;
        }
        /* модальное окно для входа/регистрации */
        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0;
            width: 100%; height: 100%;
            background: rgba(0,0,0,0.6);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }
        .modal-content {
            background: white;
            max-width: 380px;
            width: 90%;
            border-radius: 32px;
            padding: 2rem;
            text-align: center;
        }
        .modal-content input {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 60px;
        }
        .modal-buttons {
            display: flex;
            gap: 12px;
            margin-top: 16px;
            justify-content: center;
        }
        @media (max-width: 700px) {
            .header .container {
                flex-direction: column;
                align-items: center;
            }
            .auth-buttons {
                margin-top: 6px;
            }
            .logo {
                justify-content: center;
            }
        }
    </style>
</head>
<body>

<header class="header">
    <div class="container">
        <div class="logo">
            <!-- ЛОГОТИП: прямоугольник с иконкой. Вы можете заменить на <img src="ваш-логотип.png"> -->
            <div class="logo-icon" id="siteLogo">
    		<img src="лого.jpg" alt="НоваСтрой Логотип">
	    </div>
            <div class="logo-text">
                <h1>НоваСтрой</h1>
                <p>инженерное проектирование | строительные компетенции</p>
            </div>
        </div>
        <div style="display: flex; align-items: center; gap: 16px; flex-wrap: wrap;">
            <div class="nav-links">
                <a href="#" data-nav="home">Главная</a>
                <a href="#" data-module="smetnoe-delo">Сметное дело</a>
                <a href="#" data-module="upravlenie-proektami">Управление проектами</a>
                <a href="#" data-module="bim-proektirovanie">BIM проектирование</a>
                <a href="#" data-module="pozharnaya-bezopasnost">Пожарная безопасность</a>
                <a href="#" data-module="stroitelnye-materialy">Строительные материалы</a>
                <a href="#" data-module="vvedenie-v-specialnost">Введение в спец.</a>
            </div>
            <div id="auth-section" class="auth-buttons">
                <!-- динамически: кнопки входа/регистрации или профиль -->
            </div>
        </div>
    </div>
</header>

<main id="app-root" class="container">
    <div id="dynamic-content">Загрузка платформы НоваСтрой...</div>
</main>

<footer>
    <div>© 2026 год ЮГУ прототип для проектной деятельности группы СТР51б</div>
    <div class="authors-line">
        Панов И.О., Пуртов А.А., Тарасов С.И., Четвериков Н.Н., Колягин Н.Н., Пащенко В.А, Иванова К.Д.
    </div>
</footer>

<!-- Модальное окно (вход/регистрация) -->
<div id="authModal" class="modal">
    <div class="modal-content">
        <h3 id="modalTitle">Вход</h3>
        <input type="text" id="loginName" placeholder="Имя пользователя" autocomplete="off">
        <input type="password" id="loginPass" placeholder="Пароль">
        <div class="modal-buttons">
            <button id="modalActionBtn" class="btn-primary-auth">Войти</button>
            <button id="modalCloseBtn" class="btn-outline" style="background:#ddd;color:#000;">Отмена</button>
        </div>
        <p id="modalSwitchText" style="margin-top: 12px; font-size:0.8rem;">Нет аккаунта? <a href="#" id="switchToRegister">Зарегистрироваться</a></p>
    </div>
</div>

<script>
    let currentPage = 'home';
    let isLoggedIn = false;
    let currentUser = "";

    // Модули с видео и преподавателями
    const modulesData = {
        "smetnoe-delo": {
            title: "Сметное дело в строительстве",
            subtitle: "Ценообразование, нормативные базы, составление сметной документации",
            teachers: ["Панов И.О.", "Пуртов А.А.", "Тарасов С.И."],
            content: [
                { heading: "Основы ценообразования", type: "list", items: ["Сметная стоимость строительства", "Прямые и накладные расходы", "Сметная прибыль", "Индексы пересчета"] },
                { heading: "Виды смет", type: "list", items: ["Локальные сметы", "Объектные сметы", "Сводные сметные расчеты", "Ресурсный и базисно-индексный методы"] },
                { heading: "Программные комплексы", type: "text", text: "Гранд-Смета, РИК, Адепт: автоматизация расчётов, нормативная база (ГЭСН, ФЕР, ТЕР)." },
                { heading: "Практика", type: "text", text: "Рассчитайте стоимость земляных работ для котлована 10x15 м, используя ФЕР-01. Укажите состав трудозатрат." }
            ]
        },
        "upravlenie-proektami": {
            title: "Управление строительными проектами",
            subtitle: "Планирование, риски, команда, календарные графики",
            teachers: ["Четвериков Н.Н.", "Колягин Н.Н.", "Иванова К.Д."],
            content: [
                { heading: "Жизненный цикл проекта", type: "list", items: ["Инициация", "Планирование (WBS, диаграмма Ганта)", "Исполнение", "Мониторинг и контроль", "Завершение"] },
                { heading: "Инструменты PM", type: "list", items: ["MS Project", "Primavera P6", "Jira, Trello", "Канбан и Scrum в строительстве"] },
                { heading: "Управление рисками", type: "text", text: "Идентификация рисков (финансовые, технические, природные), матрица вероятности и последствий." },
                { heading: "Кейс", type: "text", text: "Разработайте фрагмент календарного графика для строительства монолитного каркаса 5-этажного здания." }
            ]
        },
        "bim-proektirovanie": {
            title: "BIM-проектирование (Building Information Modeling)",
            subtitle: "Информационное моделирование зданий, цифровые двойники",
            teachers: ["Пащенко В.А.", "Пуртов А.А.", "Четвериков Н.Н."],
            content: [
                { heading: "Уровни BIM", type: "list", items: ["BIM Level 0, 1, 2, 3", "CDE — общая среда данных", "OpenBIM и IFC формат"] },
                { heading: "Ключевое ПО", type: "list", items: ["Revit", "Navisworks", "Tekla Structures", "Renga", "ArchiCAD"] },
                { heading: "Взаимодействие дисциплин", type: "text", text: "Архитектура, конструкции, инженерные системы в единой модели. Коллизии и их разрешение." },
                { heading: "Задание", type: "text", text: "Создайте концептуальную BIM-модель простого здания в учебном ПО (или опишите алгоритм совместной работы)." }
            ]
        },
        "pozharnaya-bezopasnost": {
            title: "Пожарная безопасность и охрана труда",
            subtitle: "Нормативы, противопожарные меры, безопасность на стройплощадке",
            teachers: ["Тарасов С.И.", "Панов И.О.", "Колягин Н.Н."],
            content: [
                { heading: "Нормативная документация", type: "list", items: ["ФЗ №123", "СП 1.13130, СП 2.13130", "Правила противопожарного режима"] },
                { heading: "Системы защиты", type: "list", items: ["Автоматическая пожарная сигнализация", "Оповещение и эвакуация", "Огнетушители, дымоудаление"] },
                { heading: "Охрана труда в строительстве", type: "text", text: "Оценка рисков, СИЗ, инструктажи, безопасность на высоте." },
                { heading: "Ситуационная задача", type: "text", text: "Укажите мероприятия по пожарной безопасности на стройке с использованием открытого огня." }
            ]
        },
        "stroitelnye-materialy": {
            title: "Строительные материалы и изделия",
            subtitle: "Свойства, классификация, современные инновации",
            teachers: ["Иванова К.Д.", "Панов И.О.", "Пуртов А.А."],
            content: [
                { heading: "Основные группы материалов", type: "list", items: ["Бетон, кирпич", "Металлы, древесина", "Полимеры, композиты", "Теплоизоляция"] },
                { heading: "Физико-механические свойства", type: "list", items: ["Прочность, морозостойкость", "Водопоглощение", "Огнестойкость"] },
                { heading: "Эко-материалы и инновации", type: "text", text: "Фибробетон, газобетон, 3D-печать бетоном, переработанные композиты." },
                { heading: "Лабораторное задание", type: "text", text: "Сравните характеристики тяжелого бетона В25 и ячеистого бетона D500." }
            ]
        },
        "vvedenie-v-specialnost": {
            title: "Введение в специальность (строительство)",
            subtitle: "Профессиональная траектория, компетенции, этика",
            teachers: ["Колягин Н.Н.", "Пащенко В.А.", "Четвериков Н.Н.", "Тарасов С.И."],
            content: [
                { heading: "Ключевые роли в отрасли", type: "list", items: ["Инженер-проектировщик", "Инженер ПТО", "ГИП", "Сметчик, BIM-менеджер"] },
                { heading: "Профессиональные стандарты", type: "list", items: ["Стандарты НОСТРОЙ", "Квалификационные требования", "СРО"] },
                { heading: "Карьерный трек", type: "text", text: "От помощника до руководителя проектов. Рекомендуемые сертификации." },
                { heading: "Проектная деятельность", type: "text", text: "Освойте ЕСКД, СПДС. Разработайте личный план развития." }
            ]
        }
    };

    // Рендер авторизованной секции
    function renderAuthSection() {
        const authDiv = document.getElementById('auth-section');
        if (!authDiv) return;
        if (isLoggedIn) {
            authDiv.innerHTML = `<div class="user-greeting">👋 Привет, ${currentUser} <button class="logout-btn" id="logoutBtn">Выйти</button></div>`;
            const logoutBtn = document.getElementById('logoutBtn');
            if (logoutBtn) logoutBtn.onclick = () => { isLoggedIn = false; currentUser = ""; renderAuthSection(); render(); };
        } else {
            authDiv.innerHTML = `<button class="btn-outline" id="showLoginBtn">Войти</button><button class="btn-primary-auth" id="showRegBtn">Регистрация</button>`;
            document.getElementById('showLoginBtn')?.addEventListener('click', () => openModal('login'));
            document.getElementById('showRegBtn')?.addEventListener('click', () => openModal('register'));
        }
    }

    let modalMode = 'login';
    const modal = document.getElementById('authModal');
    function openModal(mode) {
        modalMode = mode;
        const titleEl = document.getElementById('modalTitle');
        const actionBtn = document.getElementById('modalActionBtn');
        const switchText = document.getElementById('switchToRegister');
        if (mode === 'login') {
            titleEl.innerText = 'Вход в личный кабинет';
            actionBtn.innerText = 'Войти';
            switchText.innerText = 'Нет аккаунта? Зарегистрироваться';
        } else {
            titleEl.innerText = 'Регистрация';
            actionBtn.innerText = 'Зарегистрироваться';
            switchText.innerText = 'Уже есть аккаунт? Войти';
        }
        modal.style.display = 'flex';
    }
    function closeModal() { modal.style.display = 'none'; }
    function handleAuth() {
        const username = document.getElementById('loginName').value.trim();
        const pass = document.getElementById('loginPass').value.trim();
        if (!username) { alert("Введите имя"); return; }
        if (modalMode === 'register') {
            if (pass.length < 3) { alert("Пароль минимум 3 символа"); return; }
            localStorage.setItem(`user_${username}`, pass);
            alert(`Регистрация успешна! Войдите.`);
            openModal('login');
        } else if (modalMode === 'login') {
            const savedPass = localStorage.getItem(`user_${username}`);
            if (savedPass && savedPass === pass) {
                isLoggedIn = true;
                currentUser = username;
                closeModal();
                renderAuthSection();
                render();
            } else {
                alert("Неверное имя пользователя или пароль");
            }
        }
        document.getElementById('loginName').value = '';
        document.getElementById('loginPass').value = '';
    }

    function renderHome() {
        const modulesList = [
            { id: "smetnoe-delo", title: "Сметное дело", desc: "Ценообразование, сметные нормы, автоматизация расчётов.", image: "смет.jpg", bg: "linear-gradient(135deg, #1f6e8c, #0a4b63)" },
            { id: "upravlenie-proektami", title: "Управление проектами", desc: "Планирование, риски, графики, команда.", image: "управ про.jpg", bg: "linear-gradient(135deg, #2c7c5f, #1b5d44)" },
            { id: "bim-proektirovanie", title: "BIM проектирование", desc: "Информационное моделирование, Revit, коллизии.", image: "бим.jpg", bg: "linear-gradient(135deg, #2a6f8f, #145b78)" },
            { id: "pozharnaya-bezopasnost", title: "Пожарная безопасность", desc: "Нормативы ПБ, охрана труда, системы защиты.", image: "пожар.jpg", bg: "linear-gradient(135deg, #bd6b2a, #984f16)" },
            { id: "stroitelnye-materialy", title: "Строительные материалы", desc: "Бетон, сталь, композиты, свойства.", image: "строй мат.jpg", bg: "linear-gradient(135deg, #5a6e7c, #3f5563)" },
            { id: "vvedenie-v-specialnost", title: "Введение в специальность", desc: "Траектории, компетенции, профстандарты.", image: "введение.jpg", bg: "linear-gradient(135deg, #a57348, #7b5430)" }
        ];
        const cardsHtml = modulesList.map(module => `
            <div class="module-card" data-module-id="${module.id}">
                <div class="card-img" style="background: ${module.bg}"><img src="${module.image}" class="module-icon"></div>
                <div class="card-content">
                    <h3>${module.title}</h3>
                    <p>${module.desc}</p>
                    <span class="tag">учебный модуль</span>
                    <div class="btn-module">Подробнее →</div>
                </div>
            </div>
        `).join('');
        return `
            <div class="hero-welcome">
                <h2>Обучение инженерному проектированию</h2>
                <p style="margin-top: 10px;">Модульная система: сметы, BIM, управление, безопасность, материаловедение и введение в профессию</p>
            </div>
            <div class="modules-grid">${cardsHtml}</div>
            <div class="project-authors">
                <h4>📐 Авторы образовательного прототипа</h4>
                <div class="author-names">Панов И.О. | Пуртов А.А. | Тарасов С.И. | Четвериков Н.Н. | Колягин Н.Н. | Пащенко В.А | Иванова К.Д.</div>
                <p style="margin-top: 8px;">Югорский государственный университет, проектная деятельность СТР51б</p>
            </div>
        `;
    }

    function renderModulePage(moduleId) {
        const mod = modulesData[moduleId];
        if (!mod) return `<div>Модуль не найден</div>`;
        const lessonBlocks = mod.content.map(block => {
            if (block.type === 'list') return `<div class="lesson-block"><h3>${block.heading}</h3><ul>${block.items.map(i => `<li>${i}</li>`).join('')}</ul></div>`;
            return `<div class="lesson-block"><h3>${block.heading}</h3><p>${block.text}</p></div>`;
        }).join('');
        const videoBlock = `<div class="lesson-block"><h3>🎥 Видеоурок по теме</h3><div class="video-placeholder"><span style="font-size:2rem;">📹</span><span>Видеолекция от преподавателей модуля (доступна после авторизации). Платформа поддерживает интерактивный контент.</span></div></div>`;
        const teacherBlock = `<div class="teacher-list"><span>👨‍🏫 Преподаватели модуля:</span> ${mod.teachers.join(', ')}</div>`;
        return `
            <div class="module-page">
                <div class="module-header"><h2>${mod.title}</h2><p>${mod.subtitle}</p></div>
                <div class="learning-section">${lessonBlocks}${videoBlock}${teacherBlock}</div>
                <button class="back-home-btn" id="back-to-home">← Вернуться к списку модулей</button>
            </div>
        `;
    }

    function render() {
        const contentDiv = document.getElementById('dynamic-content');
        if (!contentDiv) return;
        if (currentPage === 'home') {
            contentDiv.innerHTML = renderHome();
            attachCardListeners();
        } else if (modulesData[currentPage]) {
            contentDiv.innerHTML = renderModulePage(currentPage);
            const backBtn = document.getElementById('back-to-home');
            if (backBtn) backBtn.onclick = () => { currentPage = 'home'; render(); };
        } else { currentPage = 'home'; render(); }
        attachNavListeners();
    }

    function attachCardListeners() {
        document.querySelectorAll('.module-card').forEach(card => {
            if (card.dataset.listenerAttached === 'true') return;
            card.addEventListener('click', (e) => {
                const id = card.getAttribute('data-module-id');
                if (id && modulesData[id]) { currentPage = id; render(); }
            });
            card.dataset.listenerAttached = 'true';
        });
    }

    function attachNavListeners() {
        const homeLink = document.querySelector('[data-nav="home"]');
        if (homeLink && !homeLink.hasListener) {
            const newLink = homeLink.cloneNode(true);
            homeLink.parentNode.replaceChild(newLink, homeLink);
            newLink.addEventListener('click', (e) => { e.preventDefault(); currentPage = 'home'; render(); });
            newLink.hasListener = true;
        }
        document.querySelectorAll('[data-module]').forEach(link => {
            if (link.hasListener) return;
            const clean = link.cloneNode(true);
            link.parentNode.replaceChild(clean, link);
            clean.addEventListener('click', (e) => {
                e.preventDefault();
                const mid = clean.getAttribute('data-module');
                if (mid && modulesData[mid]) { currentPage = mid; render(); }
                else { currentPage = 'home'; render(); }
            });
            clean.hasListener = true;
        });
    }

    // Инициализация модалки и логотипа (опционально)
    document.addEventListener('DOMContentLoaded', () => {
        renderAuthSection();
        render();
        const modalClose = document.getElementById('modalCloseBtn');
        const modalAction = document.getElementById('modalActionBtn');
        const switchLink = document.getElementById('switchToRegister');
        modalClose?.addEventListener('click', closeModal);
        modalAction?.addEventListener('click', handleAuth);
        switchLink?.addEventListener('click', (e) => {
            e.preventDefault();
            modalMode = modalMode === 'login' ? 'register' : 'login';
            const title = document.getElementById('modalTitle');
            const action = document.getElementById('modalActionBtn');
            const switchT = document.getElementById('switchToRegister');
            if (modalMode === 'login') {
                title.innerText = 'Вход в личный кабинет';
                action.innerText = 'Войти';
                switchT.innerText = 'Нет аккаунта? Зарегистрироваться';
            } else {
                title.innerText = 'Регистрация';
                action.innerText = 'Зарегистрироваться';
                switchT.innerText = 'Уже есть аккаунт? Войти';
            }
        });
        window.onclick = (e) => { if (e.target === modal) closeModal(); };
        
        // Легкая подсказка: логотип можно заменить на реальную картинку
        const logoBlock = document.getElementById('siteLogo');
        if (logoBlock) {
            logoBlock.style.cursor = 'pointer';
            logoBlock.title = 'Замените этот блок на <img src=\'ваш-логотип.png\'> для реального логотипа';
        }
    });
</script>
</body>
</html>
