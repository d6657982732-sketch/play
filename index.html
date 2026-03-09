<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Лесной спавн: уровни 1-10</title>
    <style>
        body { margin: 0; overflow: hidden; font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; }
        /* Основной игровой HUD */
        #hud {
            position: absolute;
            top: 20px;
            left: 20px;
            color: #fff;
            background: rgba(30, 20, 30, 0.8);
            padding: 12px 24px;
            border-radius: 40px;
            backdrop-filter: blur(5px);
            border: 2px solid #b84aff;
            font-size: 22px;
            font-weight: bold;
            z-index: 200;
            box-shadow: 0 0 30px #b84aff80;
            text-shadow: 0 0 10px #fff;
        }
        #hud span {
            color: #ffb84a;
            margin-left: 15px;
            font-size: 28px;
        }
        #level-display {
            position: absolute;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            color: #fff;
            background: rgba(0, 20, 40, 0.8);
            padding: 10px 30px;
            border-radius: 40px;
            border: 2px solid #4ab8ff;
            font-size: 24px;
            font-weight: bold;
            z-index: 200;
            backdrop-filter: blur(5px);
            box-shadow: 0 0 30px #4ab8ff;
        }
        #health-container {
            position: absolute;
            top: 20px;
            right: 20px;
            width: 260px;
            background: rgba(20, 10, 10, 0.85);
            border-radius: 40px;
            padding: 12px 20px;
            backdrop-filter: blur(8px);
            border: 2px solid #ff4a4a;
            box-shadow: 0 0 30px #ff0000a0;
            z-index: 200;
            display: flex;
            align-items: center;
            gap: 15px;
            font-weight: bold;
        }
        #health-label {
            color: #ffaaaa;
            font-size: 20px;
            text-shadow: 0 0 8px #ff0000;
        }
        #health-bar-bg {
            flex: 1;
            height: 22px;
            background: rgba(60, 20, 20, 0.6);
            border-radius: 30px;
            overflow: hidden;
            border: 1px solid #ff8888;
        }
        #health-fill {
            height: 100%;
            width: 100%;
            background: linear-gradient(90deg, #ff8888, #ff1a1a);
            border-radius: 30px;
            transition: width 0.2s ease;
        }
        #health-value {
            color: #fff;
            font-size: 20px;
            min-width: 45px;
            text-align: right;
        }
        #scope {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 120px;
            height: 120px;
            border: 4px solid rgba(255, 255, 255, 0.9);
            border-radius: 50%;
            z-index: 150;
            pointer-events: none;
            box-shadow: 0 0 0 2px black, 0 0 30px #fff;
            background: rgba(0,0,0,0.2);
        }
        #scope::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 0;
            width: 100%;
            height: 2px;
            background: white;
            transform: translateY(-50%);
            box-shadow: 0 0 10px red;
        }
        #scope::after {
            content: '';
            position: absolute;
            left: 50%;
            top: 0;
            width: 2px;
            height: 100%;
            background: white;
            transform: translateX(-50%);
            box-shadow: 0 0 10px red;
        }
        #ammo {
            position: absolute;
            bottom: 30px;
            left: 30px;
            color: #fff;
            font-size: 28px;
            font-weight: bold;
            text-shadow: 3px 3px 0 #000;
            background: rgba(20,20,30,0.8);
            padding: 15px 30px;
            border-radius: 50px;
            border-left: 6px solid #b84aff;
            z-index: 200;
            backdrop-filter: blur(4px);
            border: 2px solid #b84aff;
            box-shadow: 0 0 20px #b84aff;
        }
        #boundary-warning {
            position: absolute;
            top: 100px;
            left: 50%;
            transform: translateX(-50%);
            color: #ffaa66;
            background: rgba(0,0,0,0.8);
            padding: 10px 20px;
            border-radius: 40px;
            font-size: 18px;
            border: 2px solid #ffaa66;
            z-index: 250;
            transition: opacity 0.3s;
            pointer-events: none;
            opacity: 0;
            font-weight: bold;
        }
        #damage-flash {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 0, 0, 0.3);
            pointer-events: none;
            z-index: 300;
            opacity: 0;
            transition: opacity 0.1s;
        }
        
        /* Меню выбора уровня */
        #menu-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 10, 0, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;
            font-family: 'Segoe UI', sans-serif;
        }
        #menu-title {
            font-size: 64px;
            font-weight: bold;
            margin-bottom: 20px;
            text-shadow: 0 0 30px #4aff4a;
            color: #aaffaa;
            letter-spacing: 4px;
        }
        #menu-subtitle {
            font-size: 24px;
            margin-bottom: 50px;
            color: #ccc;
        }
        #level-grid {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 20px;
            max-width: 800px;
            margin-bottom: 40px;
        }
        .level-btn {
            width: 100px;
            height: 100px;
            background: linear-gradient(145deg, #1a3a1a, #0a2a0a);
            border: 3px solid #4aaf4a;
            border-radius: 20px;
            color: white;
            font-size: 36px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.2s;
            box-shadow: 0 0 20px #4aaf4a80;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .level-btn:hover {
            transform: scale(1.1);
            background: #2a5a2a;
            border-color: #aaffaa;
            box-shadow: 0 0 40px #aaffaa;
        }
        .level-btn.selected {
            background: #4aaf4a;
            border-color: white;
            box-shadow: 0 0 50px #aaffaa;
        }
        #start-game-btn {
            background: linear-gradient(145deg, #4a4aff, #2a2aaf);
            border: none;
            color: white;
            font-size: 32px;
            font-weight: bold;
            padding: 20px 60px;
            border-radius: 60px;
            cursor: pointer;
            transition: all 0.2s;
            border: 3px solid #aaaaff;
            box-shadow: 0 0 40px #4a4aff;
            margin-top: 30px;
        }
        #start-game-btn:hover {
            transform: scale(1.05);
            background: #6a6aff;
            box-shadow: 0 0 70px #6a6aff;
        }
        
        /* Экран Game Over */
        #gameover-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(20, 0, 0, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1100;
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            color: white;
        }
        #gameover-title {
            font-size: 80px;
            font-weight: bold;
            color: #ff4a4a;
            text-shadow: 0 0 50px #ff0000;
            margin-bottom: 20px;
            letter-spacing: 8px;
        }
        #gameover-level {
            font-size: 28px;
            color: #ccc;
            margin-bottom: 50px;
        }
        .gameover-btn {
            background: linear-gradient(145deg, #2a2a2a, #1a1a1a);
            border: 3px solid #ff4a4a;
            color: white;
            font-size: 28px;
            font-weight: bold;
            padding: 18px 50px;
            border-radius: 60px;
            cursor: pointer;
            transition: all 0.2s;
            margin: 15px;
            min-width: 300px;
            text-align: center;
        }
        .gameover-btn:hover {
            transform: scale(1.05);
            background: #3a3a3a;
            border-color: #ff8888;
            box-shadow: 0 0 40px #ff4a4a;
        }
        #restart-btn {
            background: linear-gradient(145deg, #2a4a2a, #1a3a1a);
            border-color: #4aff4a;
        }
        #menu-btn {
            background: linear-gradient(145deg, #4a4a2a, #3a3a1a);
            border-color: #ffff4a;
        }
    </style>
</head>
<body>
    <!-- Игровой HUD (изначально скрыт, показывается после старта) -->
    <div id="hud" style="display: none;">🧟 ЗОМБИ: <span id="zombie-counter">0</span></div>
    <div id="level-display" style="display: none;">УРОВЕНЬ <span id="current-level">1</span></div>
    <div id="health-container" style="display: none;">
        <div id="health-label">❤️ ЗДОРОВЬЕ</div>
        <div id="health-bar-bg">
            <div id="health-fill" style="width:100%"></div>
        </div>
        <div id="health-value">100</div>
    </div>
    <div id="scope"></div>
    <div id="ammo" style="display: none;">🔫 AWM | Бесконечно</div>
    <div id="boundary-warning">⚠️ КРАЙ ЛЕСА</div>
    <div id="damage-flash"></div>
    <div id="controls-note" style="display: none;">
        🖱️ ЛКМ стрелять | WASD движение | Shift бег | Пробел прыжок
    </div>

    <!-- Меню выбора уровня -->
    <div id="menu-overlay">
        <div id="menu-title">ЛЕСНОЙ СПАВН</div>
        <div id="menu-subtitle">Выберите уровень (локацию)</div>
        <div id="level-grid">
            <!-- Кнопки 1-10 будут сгенерированы JS -->
        </div>
        <button id="start-game-btn">НАЧАТЬ ИГРУ</button>
    </div>

    <!-- Экран Game Over -->
    <div id="gameover-overlay">
        <div id="gameover-title">GAME OVER</div>
        <div id="gameover-level">Уровень <span id="gameover-level-num">1</span></div>
        <button class="gameover-btn" id="restart-btn">🔄 НАЧАТЬ ЗАНОВО</button>
        <button class="gameover-btn" id="menu-btn">🏠 ВЕРНУТЬСЯ В МЕНЮ</button>
    </div>

    <script type="importmap">
        {
            "imports": {
                "three": "https://unpkg.com/three@0.126.0/build/three.module.js",
                "three/addons/": "https://unpkg.com/three@0.126.0/examples/jsm/"
            }
        }
    </script>

    <script type="module">
        import * as THREE from 'three';
        import { PointerLockControls } from 'three/addons/controls/PointerLockControls.js';

        // --- ГЛОБАЛЬНЫЕ ПЕРЕМЕННЫЕ ---
        let currentLevel = 1;
        let gameActive = false;
        let scene, camera, renderer, controls;
        let moonLight, ambientLight;
        let ground, moon, stars, grass, trees, bushes;
        let awmGroup;
        let zombies = [];
        let attackCooldowns = new Map();
        
        // Настройки
        const WORLD_BOUNDARY = 24;
        const PLAYER_SPEED_NORMAL = 8.5;
        const PLAYER_SPEED_BOOST = 16;
        const ZOMBIE_DAMAGE = 15;
        const PLAYER_MAX_HEALTH = 100;
        const ZOMBIE_ATTACK_COOLDOWN = 1000;
        
        // Состояние игрока
        let playerHealth = PLAYER_MAX_HEALTH;
        
        // Управление
        const moveState = { forward: false, backward: false, left: false, right: false, shift: false };
        const velocity = new THREE.Vector3();

        // --- ЭЛЕМЕНТЫ ИНТЕРФЕЙСА ---
        const hud = document.getElementById('hud');
        const levelDisplay = document.getElementById('level-display');
        const healthContainer = document.getElementById('health-container');
        const ammoDiv = document.getElementById('ammo');
        const controlsNote = document.getElementById('controls-note');
        const menuOverlay = document.getElementById('menu-overlay');
        const gameoverOverlay = document.getElementById('gameover-overlay');
        const zombieCounter = document.getElementById('zombie-counter');
        const healthFill = document.getElementById('health-fill');
        const healthValue = document.getElementById('health-value');
        const currentLevelSpan = document.getElementById('current-level');
        const gameoverLevelSpan = document.getElementById('gameover-level-num');
        const damageFlash = document.getElementById('damage-flash');
        const boundaryWarning = document.getElementById('boundary-warning');
        const levelGrid = document.getElementById('level-grid');
        const startGameBtn = document.getElementById('start-game-btn');
        const restartBtn = document.getElementById('restart-btn');
        const menuBtn = document.getElementById('menu-btn');

        // --- ГЕНЕРАЦИЯ КНОПОК УРОВНЕЙ 1-10 ---
        for (let i = 1; i <= 10; i++) {
            const btn = document.createElement('div');
            btn.className = 'level-btn';
            btn.textContent = i;
            btn.dataset.level = i;
            btn.addEventListener('click', () => {
                document.querySelectorAll('.level-btn').forEach(b => b.classList.remove('selected'));
                btn.classList.add('selected');
                currentLevel = i;
            });
            levelGrid.appendChild(btn);
        }
        // Выбираем уровень 1 по умолчанию
        document.querySelector('.level-btn').classList.add('selected');

        // --- ФУНКЦИИ ИНИЦИАЛИЗАЦИИ ИГРЫ ---
        function initGame() {
            // Скрываем меню, показываем HUD
            menuOverlay.style.display = 'none';
            gameoverOverlay.style.display = 'none';
            hud.style.display = 'block';
            levelDisplay.style.display = 'block';
            healthContainer.style.display = 'flex';
            ammoDiv.style.display = 'block';
            controlsNote.style.display = 'block';
            
            currentLevelSpan.textContent = currentLevel;
            
            // Сброс здоровья
            playerHealth = PLAYER_MAX_HEALTH;
            updateHealth();
            
            // Создаем сцену заново (или очищаем)
            if (scene) {
                // Полная перезагрузка страницы проще, но мы сделаем аккуратную очистку
                // Однако для простоты используем location.reload() для чистой инициализации
                // Но чтобы не перезагружать, мы пересоздадим сцену
                location.reload(); // Временно для надежности, но можно и без перезагрузки
                return;
            }
            
            // Инициализация Three.js
            scene = new THREE.Scene();
            scene.background = new THREE.Color(0x0a1420);
            scene.fog = new THREE.Fog(0x1a2a2a, 30, 70);

            camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
            camera.position.set(5, 2, 8);

            renderer = new THREE.WebGLRenderer({ antialias: true });
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.shadowMap.enabled = true;
            renderer.shadowMap.type = THREE.PCFSoftShadowMap;
            document.body.appendChild(renderer.domElement);

            // Освещение
            moonLight = new THREE.DirectionalLight(0xaaccff, 0.9);
            moonLight.position.set(-20, 25, -15);
            moonLight.castShadow = true;
            moonLight.receiveShadow = true;
            moonLight.shadow.mapSize.width = 1024;
            moonLight.shadow.mapSize.height = 1024;
            moonLight.shadow.camera.near = 1;
            moonLight.shadow.camera.far = 70;
            moonLight.shadow.camera.left = -30;
            moonLight.shadow.camera.right = 30;
            moonLight.shadow.camera.top = 30;
            moonLight.shadow.camera.bottom = -30;
            scene.add(moonLight);

            ambientLight = new THREE.AmbientLight(0x335588, 0.7);
            scene.add(ambientLight);

            // Земля
            const groundGeometry = new THREE.CircleGeometry(80, 64);
            const groundMaterial = new THREE.MeshStandardMaterial({ color: 0x1a3a1a, roughness: 0.9 });
            ground = new THREE.Mesh(groundGeometry, groundMaterial);
            ground.rotation.x = -Math.PI / 2;
            ground.position.y = 0;
            ground.receiveShadow = true;
            scene.add(ground);

            // Луна
            moon = new THREE.Mesh(
                new THREE.SphereGeometry(2, 32),
                new THREE.MeshStandardMaterial({ color: 0xfff5d1, emissive: 0x332211 })
            );
            moon.position.set(30, 25, -40);
            scene.add(moon);

            // Звезды
            const starsGeo = new THREE.BufferGeometry();
            const starsPos = [];
            for (let i = 0; i < 1000; i++) {
                const r = 100 + Math.random() * 100;
                const theta = Math.random() * Math.PI * 2;
                const phi = Math.acos(2 * Math.random() - 1);
                starsPos.push(
                    Math.sin(phi) * Math.cos(theta) * r,
                    Math.sin(phi) * Math.sin(theta) * r,
                    Math.cos(phi) * r
                );
            }
            starsGeo.setAttribute('position', new THREE.Float32BufferAttribute(starsPos, 3));
            stars = new THREE.Points(starsGeo, new THREE.PointsMaterial({ color: 0xffffff, size: 0.2 }));
            scene.add(stars);

            // Трава
            const grassGeo = new THREE.BufferGeometry();
            const grassPos = [];
            for (let i = 0; i < 2000; i++) {
                const r = WORLD_BOUNDARY * Math.sqrt(Math.random());
                const a = Math.random() * Math.PI * 2;
                grassPos.push(Math.cos(a) * r, 0, Math.sin(a) * r);
            }
            grassGeo.setAttribute('position', new THREE.Float32BufferAttribute(grassPos, 3));
            grass = new THREE.Points(grassGeo, new THREE.PointsMaterial({ color: 0x3a6a3a, size: 0.15 }));
            scene.add(grass);

            // Деревья
            function createTree(x, z) {
                const group = new THREE.Group();
                const trunk = new THREE.Mesh(
                    new THREE.CylinderGeometry(0.5, 0.7, 2.5),
                    new THREE.MeshStandardMaterial({ color: 0x5a4030 })
                );
                trunk.position.y = 1.25;
                trunk.castShadow = true;
                trunk.receiveShadow = true;
                group.add(trunk);
                
                const leafMat = new THREE.MeshStandardMaterial({ color: 0x1a4a1a });
                const leaf1 = new THREE.Mesh(new THREE.ConeGeometry(1.2, 1.8), leafMat);
                leaf1.position.y = 2.5;
                leaf1.castShadow = true;
                group.add(leaf1);
                const leaf2 = new THREE.Mesh(new THREE.ConeGeometry(0.9, 1.4), leafMat);
                leaf2.position.y = 3.8;
                leaf2.castShadow = true;
                group.add(leaf2);
                
                group.position.set(x, 0, z);
                return group;
            }

            trees = [];
            for (let i = 0; i < 50; i++) {
                const a = Math.random() * Math.PI * 2;
                const d = 4 + Math.random() * (WORLD_BOUNDARY - 3);
                const tree = createTree(Math.cos(a) * d, Math.sin(a) * d);
                scene.add(tree);
                trees.push(tree);
            }
            scene.add(createTree(3, 2));
            scene.add(createTree(-2, 4));

            // Кусты
            bushes = [];
            for (let i = 0; i < 30; i++) {
                const r = 3 + Math.random() * (WORLD_BOUNDARY - 3);
                const a = Math.random() * Math.PI * 2;
                const x = Math.cos(a) * r;
                const z = Math.sin(a) * r;
                const bush = new THREE.Mesh(
                    new THREE.SphereGeometry(0.4, 4),
                    new THREE.MeshStandardMaterial({ color: 0x2a5a2a })
                );
                bush.position.set(x, 0.2, z);
                bush.castShadow = true;
                bush.receiveShadow = true;
                scene.add(bush);
                bushes.push(bush);
            }

            // AWM
            awmGroup = new THREE.Group();
            
            const barrel = new THREE.Mesh(
                new THREE.CylinderGeometry(0.12, 0.12, 2.2),
                new THREE.MeshStandardMaterial({ color: 0x222222, metalness: 0.9, roughness: 0.3 })
            );
            barrel.rotation.x = Math.PI/2;
            barrel.position.set(0, 0, -1.4);
            barrel.castShadow = true;
            awmGroup.add(barrel);

            const body = new THREE.Mesh(
                new THREE.BoxGeometry(0.25, 0.25, 1.0),
                new THREE.MeshStandardMaterial({ color: 0x3a4a3a, roughness: 0.6 })
            );
            body.position.set(0, 0, -0.2);
            body.castShadow = true;
            awmGroup.add(body);

            const grip = new THREE.Mesh(
                new THREE.BoxGeometry(0.18, 0.4, 0.3),
                new THREE.MeshStandardMaterial({ color: 0x2a1a0a })
            );
            grip.position.set(0, -0.2, 0.2);
            grip.castShadow = true;
            awmGroup.add(grip);

            const mag = new THREE.Mesh(
                new THREE.BoxGeometry(0.2, 0.3, 0.3),
                new THREE.MeshStandardMaterial({ color: 0x111111, metalness: 0.8 })
            );
            mag.position.set(0, -0.25, 0.1);
            mag.castShadow = true;
            awmGroup.add(mag);

            const scopeBase = new THREE.Mesh(
                new THREE.CylinderGeometry(0.2, 0.2, 0.4),
                new THREE.MeshStandardMaterial({ color: 0x333333 })
            );
            scopeBase.rotation.x = Math.PI/2;
            scopeBase.position.set(0, 0.15, -0.6);
            scopeBase.castShadow = true;
            awmGroup.add(scopeBase);

            const scopeLens = new THREE.Mesh(
                new THREE.CylinderGeometry(0.1, 0.1, 0.1),
                new THREE.MeshStandardMaterial({ color: 0x88aaff, emissive: 0x112233 })
            );
            scopeLens.rotation.x = Math.PI/2;
            scopeLens.position.set(0, 0.15, -0.4);
            scopeLens.castShadow = true;
            awmGroup.add(scopeLens);

            const bipod = new THREE.Mesh(
                new THREE.BoxGeometry(0.1, 0.3, 0.2),
                new THREE.MeshStandardMaterial({ color: 0x444444 })
            );
            bipod.position.set(0.15, -0.2, -1.0);
            bipod.castShadow = true;
            awmGroup.add(bipod);

            awmGroup.position.set(0.25, -0.15, -0.6);
            awmGroup.rotation.y = 0.1;
            awmGroup.rotation.x = 0.1;
            camera.add(awmGroup);
            scene.add(camera);

            // Управление
            controls = new PointerLockControls(camera, document.body);
            
            // Зомби (в зависимости от уровня)
            zombies = [];
            attackCooldowns.clear();
            
            const zombieCount = Math.min(5 + currentLevel, 15); // от 6 до 15
            for (let i = 0; i < zombieCount; i++) {
                const angle = Math.random() * Math.PI * 2;
                const dist = 5 + Math.random() * 15;
                const x = Math.cos(angle) * dist;
                const z = Math.sin(angle) * dist;
                const zom = createZombie(x, z);
                scene.add(zom);
                zombies.push({ mesh: zom, health: 1 });
                attackCooldowns.set(zom, 0);
            }
            
            updateCounter();
            
            // Запуск анимации
            animate();
        }

        function createZombie(x, z) {
            const group = new THREE.Group();
            
            const body = new THREE.Mesh(
                new THREE.CylinderGeometry(0.4, 0.5, 1.3),
                new THREE.MeshStandardMaterial({ color: 0x2a4a2a, emissive: 0x0a1a0a })
            );
            body.position.y = 0.65;
            body.castShadow = true;
            body.receiveShadow = true;
            group.add(body);
            
            const head = new THREE.Mesh(
                new THREE.SphereGeometry(0.3),
                new THREE.MeshStandardMaterial({ color: 0x4a5a4a })
            );
            head.position.y = 1.4;
            head.castShadow = true;
            head.receiveShadow = true;
            group.add(head);
            
            const eyeMat = new THREE.MeshStandardMaterial({ color: 0xff0000, emissive: 0x330000 });
            const eyeL = new THREE.Mesh(new THREE.SphereGeometry(0.08), eyeMat);
            eyeL.position.set(-0.12, 1.5, 0.25);
            group.add(eyeL);
            const eyeR = new THREE.Mesh(new THREE.SphereGeometry(0.08), eyeMat);
            eyeR.position.set(0.12, 1.5, 0.25);
            group.add(eyeR);
            
            group.position.set(x, 0, z);
            return group;
        }

        // --- ФУНКЦИИ ОБНОВЛЕНИЯ HUD ---
        function updateCounter() {
            const alive = zombies.filter(z => z.health > 0).length;
            zombieCounter.textContent = alive;
        }

        function updateHealth() {
            const percent = (playerHealth / PLAYER_MAX_HEALTH) * 100;
            healthFill.style.width = percent + '%';
            healthValue.textContent = Math.floor(playerHealth);
        }

        // --- ИГРОВОЙ ЦИКЛ ---
        function animate() {
            if (!scene) return;
            
            requestAnimationFrame(animate);
            
            if (controls && controls.isLocked && playerHealth > 0) {
                updatePlayerMovement();
                animateZombies();
                applyZombieDamage();
            }
            
            if (renderer && scene && camera) {
                renderer.render(scene, camera);
            }
        }

        function updatePlayerMovement() {
            if (!controls || !controls.isLocked || playerHealth <= 0) return;
            
            velocity.x -= velocity.x * 0.12;
            velocity.z -= velocity.z * 0.12;
            
            const currentSpeed = moveState.shift ? PLAYER_SPEED_BOOST : PLAYER_SPEED_NORMAL;
            const moveX = (moveState.right ? 1 : 0) - (moveState.left ? 1 : 0);
            const moveZ = (moveState.forward ? 1 : 0) - (moveState.backward ? 1 : 0);
            
            if (moveZ !== 0) velocity.z += moveZ * currentSpeed * 0.015;
            if (moveX !== 0) velocity.x += moveX * currentSpeed * 0.015;
            
            controls.moveRight(velocity.x);
            controls.moveForward(velocity.z);
            
            camera.position.y = 2;
            
            applyBoundary();
        }

        function animateZombies() {
            const zombieSpeed = 0.025;
            zombies.forEach(z => {
                if (z.health <= 0) return;
                
                const dir = new THREE.Vector3().subVectors(camera.position, z.mesh.position);
                dir.y = 0;
                
                if (dir.length() > 0.1) {
                    dir.normalize();
                    z.mesh.position.x += dir.x * zombieSpeed;
                    z.mesh.position.z += dir.z * zombieSpeed;
                    
                    const angle = Math.atan2(dir.x, dir.z);
                    z.mesh.rotation.y = angle;
                }
            });
        }

        function applyZombieDamage() {
            const now = Date.now();
            zombies.forEach(z => {
                if (z.health <= 0) return;
                
                const dist = camera.position.distanceTo(z.mesh.position);
                if (dist < 1.2 && now - (attackCooldowns.get(z.mesh) || 0) > ZOMBIE_ATTACK_COOLDOWN) {
                    playerHealth = Math.max(0, playerHealth - ZOMBIE_DAMAGE);
                    updateHealth();
                    
                    damageFlash.style.opacity = '1';
                    setTimeout(() => damageFlash.style.opacity = '0', 150);
                    
                    const dir = new THREE.Vector3().subVectors(camera.position, z.mesh.position).normalize();
                    camera.position.x += dir.x * 1.2;
                    camera.position.z += dir.z * 1.2;
                    
                    attackCooldowns.set(z.mesh, now);
                    
                    if (playerHealth <= 0) {
                        gameOver();
                    }
                }
            });
        }

        function applyBoundary() {
            const pos = camera.position;
            const dist = Math.sqrt(pos.x*pos.x + pos.z*pos.z);
            
            if (dist > WORLD_BOUNDARY) {
                const angle = Math.atan2(pos.x, pos.z);
                camera.position.x = Math.sin(angle) * WORLD_BOUNDARY * 0.98;
                camera.position.z = Math.cos(angle) * WORLD_BOUNDARY * 0.98;
                
                boundaryWarning.style.opacity = '1';
                clearTimeout(window.boundaryTimeout);
                window.boundaryTimeout = setTimeout(() => boundaryWarning.style.opacity = '0', 800);
            }
        }

        function gameOver() {
            controls.unlock();
            gameoverLevelSpan.textContent = currentLevel;
            gameoverOverlay.style.display = 'flex';
        }

        // --- ОБРАБОТЧИКИ СОБЫТИЙ ---
        document.addEventListener('keydown', (e) => {
            if (!controls || !controls.isLocked) return;
            switch(e.code) {
                case 'KeyW': moveState.forward = true; break;
                case 'KeyS': moveState.backward = true; break;
                case 'KeyA': moveState.left = true; break;
                case 'KeyD': moveState.right = true; break;
                case 'ShiftLeft': moveState.shift = true; break;
                case 'Space': if (controls.isLocked) camera.position.y += 0.6; break;
            }
        });
        
        document.addEventListener('keyup', (e) => {
            switch(e.code) {
                case 'KeyW': moveState.forward = false; break;
                case 'KeyS': moveState.backward = false; break;
                case 'KeyA': moveState.left = false; break;
                case 'KeyD': moveState.right = false; break;
                case 'ShiftLeft': moveState.shift = false; break;
            }
        });

        document.addEventListener('click', () => {
            if (controls && !controls.isLocked && playerHealth > 0 && gameoverOverlay.style.display !== 'flex') {
                controls.lock();
            }
        });

        document.addEventListener('mousedown', (e) => {
            if (e.button !== 0 || !controls || !controls.isLocked || playerHealth <= 0) return;
            
            if (awmGroup) {
                awmGroup.position.z += 0.15;
                setTimeout(() => awmGroup.position.z -= 0.15, 60);
            }

            const raycaster = new THREE.Raycaster();
            raycaster.ray.origin.copy(camera.position);
            raycaster.ray.direction.copy(camera.getWorldDirection(new THREE.Vector3()));
            
            const targets = zombies.filter(z => z.health > 0).map(z => z.mesh);
            const intersects = raycaster.intersectObjects(targets, true);
            
            if (intersects.length > 0) {
                let hitObj = intersects[0].object;
                while (hitObj.parent && !zombies.some(z => z.mesh === hitObj)) {
                    hitObj = hitObj.parent;
                }
                const zombieEntry = zombies.find(z => z.mesh === hitObj);
                if (zombieEntry) {
                    zombieEntry.health = 0;
                    scene.remove(zombieEntry.mesh);
                    updateCounter();
                }
            }
        });

        // --- КНОПКИ МЕНЮ ---
        startGameBtn.addEventListener('click', () => {
            initGame();
        });

        restartBtn.addEventListener('click', () => {
            gameoverOverlay.style.display = 'none';
            initGame();
        });

        menuBtn.addEventListener('click', () => {
            gameoverOverlay.style.display = 'none';
            menuOverlay.style.display = 'flex';
            hud.style.display = 'none';
            levelDisplay.style.display = 'none';
            healthContainer.style.display = 'none';
            ammoDiv.style.display = 'none';
            controlsNote.style.display = 'none';
            location.reload(); // Простой способ сбросить сцену
        });

        window.addEventListener('resize', () => {
            if (camera && renderer) {
                camera.aspect = window.innerWidth / window.innerHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(window.innerWidth, window.innerHeight);
            }
        });
    </script>
</body>
</html>
