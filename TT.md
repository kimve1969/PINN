<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Техническое задание (ТЗ) на поставку вычислительного узла</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Roboto, Arial, sans-serif;
            background: #f2f4f8;
            padding: 40px 20px;
            display: flex;
            justify-content: center;
        }
        .document {
            max-width: 1100px;
            width: 100%;
            background: #ffffff;
            padding: 50px 60px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
            border-radius: 8px;
        }
        h1 {
            font-size: 28px;
            text-align: center;
            border-bottom: 3px solid #1a3b5d;
            padding-bottom: 18px;
            margin-bottom: 30px;
            color: #1a3b5d;
            letter-spacing: 0.5px;
        }
        .meta {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            background: #f8faff;
            padding: 15px 20px;
            border-radius: 6px;
            margin-bottom: 30px;
            border-left: 5px solid #1a3b5d;
            font-size: 15px;
        }
        .meta span {
            font-weight: 600;
            color: #1a3b5d;
        }
        h2 {
            font-size: 20px;
            color: #1a3b5d;
            margin-top: 30px;
            margin-bottom: 12px;
            border-bottom: 1px solid #dce1ec;
            padding-bottom: 6px;
        }
        h3 {
            font-size: 17px;
            color: #2c3e50;
            margin-top: 20px;
            margin-bottom: 8px;
        }
        p, li {
            font-size: 15px;
            line-height: 1.6;
            color: #1e2a3a;
        }
        ul, ol {
            padding-left: 26px;
            margin: 10px 0 16px 0;
        }
        li {
            margin-bottom: 4px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 14px 0 18px 0;
            font-size: 14px;
        }
        th {
            background: #e8edf5;
            color: #1a3b5d;
            font-weight: 600;
            padding: 10px 12px;
            border: 1px solid #c6d0df;
            text-align: left;
        }
        td {
            padding: 9px 12px;
            border: 1px solid #c6d0df;
            vertical-align: top;
        }
        .badge {
            display: inline-block;
            background: #d32f2f;
            color: #fff;
            font-weight: 700;
            font-size: 12px;
            padding: 2px 10px;
            border-radius: 20px;
            margin-left: 6px;
            letter-spacing: 0.3px;
            text-transform: uppercase;
        }
        .badge-success {
            background: #2e7d32;
        }
        .critical {
            background: #fff5f5;
            border-left: 5px solid #c62828;
            padding: 14px 18px;
            margin: 18px 0;
            border-radius: 4px;
        }
        .critical strong {
            color: #b71c1c;
        }
        .checklist {
            list-style: none;
            padding-left: 0;
        }
        .checklist li {
            padding: 6px 0 6px 32px;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="%231a3b5d" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2"/></svg>') left center no-repeat;
            background-size: 18px;
        }
        .checklist li.done {
            background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="%232e7d32" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2" stroke="%232e7d32"/><path d="M9 12l2 2 4-4" stroke="%232e7d32" stroke-width="3"/></svg>');
        }
        .signatures {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-top: 40px;
            padding-top: 30px;
            border-top: 2px dashed #b0bec5;
        }
        .signature-block {
            width: 42%;
            min-width: 200px;
        }
        .signature-block p {
            margin: 6px 0;
            font-size: 15px;
        }
        .signature-line {
            border-bottom: 1px solid #1a3b5d;
            width: 100%;
            margin-top: 16px;
            margin-bottom: 6px;
        }
        .footer-note {
            margin-top: 30px;
            font-size: 13px;
            color: #6b7a8f;
            text-align: center;
            border-top: 1px solid #e0e6ef;
            padding-top: 20px;
        }
        @media (max-width: 700px) {
            .document { padding: 20px; }
            .meta { flex-direction: column; gap: 6px; }
            .signature-block { width: 100%; margin-bottom: 25px; }
        }
        .print-only {
            display: none;
        }
        @media print {
            body { background: white; padding: 0; }
            .document { box-shadow: none; border-radius: 0; padding: 30px; }
            .badge { -webkit-print-color-adjust: exact; print-color-adjust: exact; }
        }
    </style>
</head>
<body>
<div class="document">

    <!-- ЗАГОЛОВОК -->
    <h1>ТЕХНИЧЕСКОЕ ЗАДАНИЕ (ТЗ) <br>НА ПОСТАВКУ ВЫЧИСЛИТЕЛЬНОГО УЗЛА ДЛЯ HPC-НАГРУЗОК И ОБУЧЕНИЯ НЕЙРОСЕТЕЙ</h1>

    <!-- МЕТАДАННЫЕ -->
    <div class="meta">
        <div><span>Версия:</span> 1.0</div>
        <div><span>Дата:</span> «___» __________ 2026 г.</div>
        <div><span>Статус:</span> Обязательно к исполнению поставщиком</div>
    </div>

    <!-- 1. ТЕРМИНЫ -->
    <h2>1. Термины и определения</h2>
    <table>
        <tr><th>Термин</th><th>Определение</th></tr>
        <tr><td><strong>УЗЕЛ</strong></td><td>Физический сервер, содержащий один или несколько CPU для оркестрации вычислений и один или несколько GPU для выполнения вычислений.</td></tr>
        <tr><td><strong>ПАК</strong></td><td>Совокупность из одного или нескольких УЗЛОВ. Должна иметь возможность масштабирования (наращивания) вычислительной мощности двумя способами: (1) увеличение числа GPU внутри одного УЗЛА, (2) увеличение числа УЗЛОВ в ПАКЕ.</td></tr>
        <tr><td><strong>DDP</strong></td><td>Distributed Data Parallel — технология распределённого обучения PyTorch с использованием бэкенда NCCL.</td></tr>
        <tr><td><strong>RDMA</strong></td><td>Remote Direct Memory Access — прямой доступ к памяти удалённого устройства без участия CPU.</td></tr>
        <tr><td><strong>Zero-Copy</strong></td><td>Передача данных из памяти GPU в сетевой адаптер минуя системную память и CPU.</td></tr>
    </table>

    <!-- 2. САЙЗИНГ -->
    <h2>2. Минимальная конфигурация поставки (Сайзинг)</h2>
    <table>
        <tr><th>Параметр</th><th>Значение</th></tr>
        <tr><td>Количество УЗЛОВ в поставке</td><td>1 (один)</td></tr>
        <tr><td>Минимальное количество GPU в УЗЛЕ</td><td>2 (два)</td></tr>
        <tr><td>Требование к масштабируемости</td><td>Архитектура должна позволять расширение до 8 GPU внутри УЗЛА и объединение минимум 2 УЗЛОВ в ПАК без замены материнских плат и сетевых коммутаторов (поставщик предоставляет схему коммутации).</td></tr>
    </table>

    <!-- 3. GPU -->
    <h2>3. Требования к GPU (аппаратная поддержка форматов)</h2>
    <p>Поставщик обязан предоставить паспортные значения пиковой производительности для каждого формата:</p>
    <table>
        <tr><th>Формат</th><th>Поддержка (обязательно)</th><th>Пиковая производительность</th></tr>
        <tr><td>FP64 (двойная точность)</td><td><strong>ДА</strong></td><td>_________ Тфлопс</td></tr>
        <tr><td>FP32 (одинарная точность)</td><td><strong>ДА</strong></td><td>_________ Тфлопс</td></tr>
        <tr><td>FP16 (половинная точность)</td><td><strong>ДА</strong></td><td>_________ Тфлопс</td></tr>
        <tr><td>INT8 (целочисленный 8 бит)</td><td><strong>ДА</strong></td><td>_________ Топс</td></tr>
        <tr><td>INT4 (целочисленный 4 бит)</td><td><strong>ДА</strong></td><td>_________ Топс</td></tr>
    </table>

    <!-- 4. КОММУНИКАЦИИ -->
    <h2>4. Требования к коммуникациям (RDMA и Zero-Copy)</h2>
    <h3>4.1. Внутри УЗЛА</h3>
    <ul>
        <li>Сквозная поддержка RDMA между любыми GPU через высокоскоростной интерконнект (NVLink / Infinity Fabric).</li>
        <li>Прямой доступ к памяти соседнего GPU без копирования в RAM CPU.</li>
    </ul>
    <h3>4.2. Между УЗЛАМИ</h3>
    <ul>
        <li>На каждом УЗЛЕ установлен сетевой адаптер с поддержкой <strong>GPUDirect RDMA</strong> (ConnectX-7 / BlueField или аналог).</li>
        <li>Аппаратная поддержка передачи данных из памяти GPU в сетевой адаптер <strong>без участия CPU</strong> (Zero-Copy).</li>
    </ul>
    <h3>4.3. Подтверждение</h3>
    <ul>
        <li>Топологическая карта шин PCIe с указанием маршрутов GPU → сетевой адаптер.</li>
        <li>Результат команды <code>nvidia-smi topo -m</code> (NVIDIA) или <code>rocm-smi --topo</code> (AMD).</li>
    </ul>

    <!-- 5. MPI -->
    <h2>5. Требования к аппаратно-ускоренным коллективным MPI-операциям</h2>
    <p>Предустанавливается библиотека коллективных коммуникаций (NCCL / RCCL) с поддержкой RDMA для операций:</p>
    <ul>
        <li><strong>All-Reduce</strong> — ДА</li>
        <li><strong>All-Gather</strong> — ДА</li>
        <li><strong>Reduce-Scatter</strong> — ДА</li>
        <li><strong>Broadcast</strong> — ДА</li>
    </ul>
    <h3>5.1. Автоматический выбор топологии</h3>
    <ul>
        <li><strong>Ring</strong> — для больших сообщений (&gt; 1 МБ).</li>
        <li><strong>Tree</strong> — для малых сообщений (&lt; 256 КБ).</li>
        <li><strong>Hierarchical</strong> — гибридная (NVLink внутри узла, сеть между узлами).</li>
    </ul>
    <h3>5.2. Приёмочные тесты</h3>
    <ul>
        <li>OSU Micro-Benchmarks (<code>osu_allreduce</code>, <code>osu_bcast</code>, <code>osu_allgather</code>).</li>
        <li>NCCL-Tests (<code>all_reduce_perf</code>, <code>all_gather_perf</code>).</li>
    </ul>
    <p><strong>Критерий:</strong> Реальная пропускная способность (GB/s) и задержка (μs) — отклонение <strong>не более 10%</strong> от паспортных значений.</p>

    <!-- 6. ПРОГРАММНЫЙ СТЕК -->
    <h2>6. Требования к программному стеку (полный список)</h2>
    <h3>6.1. Системное ПО</h3>
    <ul>
        <li>ОС: Ubuntu 22.04 LTS / RHEL 9 с ядром, сертифицированным производителем GPU.</li>
        <li>Оригинальные драйверы производителя с флагом <code>NVreg_EnableGpuDirect=1</code> (для NVIDIA).</li>
    </ul>
    <h3>6.2. Библиотеки исполнения</h3>
    <table>
        <tr><th>Компонент</th><th>Назначение</th></tr>
        <tr><td>CUDA Toolkit / ROCm</td><td>Базовый стек</td></tr>
        <tr><td>cuBLAS / rocBLAS</td><td>Линейная алгебра</td></tr>
        <tr><td>cuFFT / rocFFT</td><td>Быстрое преобразование Фурье</td></tr>
        <tr><td>cuSPARSE / rocSPARSE</td><td>Разреженные матрицы</td></tr>
    </table>
    <h3>6.3. Среда разработчика (Python)</h3>
    <ul>
        <li>Python 3.10+</li>
        <li>PyTorch + TensorFlow (последние стабильные версии под CUDA/ROCm)</li>
        <li><strong>CUDA Python</strong> (пакет <code>cuda-python</code>) — <span class="badge">ОБЯЗАТЕЛЬНО</span></li>
        <li>NumPy, Pandas, Scikit-learn</li>
        <li>Jupyter Notebook / Lab</li>
        <li><strong>DeepXDE</strong> — обязательная установка и проверка запуска на GPU</li>
    </ul>
    <h3>6.4. Распределённое обучение (DDP)</h3>
    <ul>
        <li><code>torch.distributed</code> с бэкендом <strong>NCCL</strong></li>
        <li>Переменные окружения: <code>NCCL_IB_DISABLE=0</code>, <code>NCCL_SOCKET_IFNAME</code> (указан интерфейс), <code>NCCL_DEBUG=INFO</code></li>
    </ul>
    <h3>6.5. Оркестрация и мониторинг</h3>
    <ul>
        <li><strong>Планировщик:</strong> Slurm с поддержкой Gres (GPU) + Pyxis</li>
        <li><strong>Мониторинг:</strong> Grafana + Prometheus (CPU, GPU загрузка/температура/VRAM, сеть). Алерты при превышении 80°C.</li>
        <li><strong>Контейнеризация:</strong> Docker + Kubernetes + Singularity/Apptainer с пробросом GPU</li>
    </ul>

    <!-- 7. ОБЯЗАТЕЛЬСТВА -->
    <h2>7. Обязательства поставщика «под ключ»</h2>
    <ul>
        <li>Монтаж оборудования в стойку (если предусмотрено).</li>
        <li>Установка и настройка всего ПО из раздела 6.</li>
        <li>Настройка сети и RDMA.</li>
        <li>Предоставление писем совместимости от производителя GPU для PyTorch и TensorFlow.</li>
        <li>Создание скрипта <code>final_test.sh</code>, запускающего все тесты приёмки со статусом PASS/FAIL.</li>
    </ul>

    <!-- 8. ПРИЁМКА -->
    <h2>8. Сценарий приёмки (чек-лист)</h2>
    <p>Пункты с пометкой <span class="badge">КРИТИЧНО</span> являются обязательными. При невыполнении любого из них приёмка останавливается.</p>
    <ul class="checklist">
        <li><strong>Визуальный осмотр:</strong> В УЗЛЕ установлено ≥ 2 GPU.</li>
        <li><strong>FP64:</strong> Тест двойной точности даёт эталонный результат.</li>
        <li><strong>RDMA внутри УЗЛА:</strong> В <code>nvidia-smi topo -m</code> виден NVLink.</li>
        <li class="critical"><strong>Zero-Copy:</strong> В логах NCCL присутствует <code>Using network: IB/RoCE</code> (не Socket). <span class="badge">КРИТИЧНО</span></li>
        <li><strong>MPI-тесты:</strong> OSU All-Reduce на 2 GPU показывает задержку &lt; 10 мкс.</li>
        <li class="critical"><strong>CUDA Python:</strong> Импорт <code>cuda</code> и вызов драйвера работают. <span class="badge">КРИТИЧНО</span></li>
        <li class="critical"><strong>DDP инициализация:</strong> <code>torch.distributed</code> с бэкендом <code>nccl</code> поднимается без ошибок. <span class="badge">КРИТИЧНО</span></li>
        <li><strong>DDP All-Reduce:</strong> Тест на 2 GPU выдаёт математически верный результат (сумма = 3.0).</li>
        <li><strong>Логи NCCL:</strong> При запуске DDP видны строки <code>Using NVLink</code> и <code>Ring/Trees</code>.</li>
        <li><strong>Slurm:</strong> Команда <code>srun --gres=gpu:2 nvidia-smi</code> выделяет оба GPU.</li>
        <li><strong>Мониторинг:</strong> Панель показывает графики температуры при нагрузке.</li>
        <li><strong>DeepXDE:</strong> Пример решения уравнения Бюргерса на GPU завершён без ошибок.</li>
        <li><strong>Масштабируемость DDP:</strong> Время одной эпохи на 2 GPU минимум в 1.5 раза меньше, чем на 1 GPU.</li>
    </ul>

    <!-- 9. БРАКОВКА -->
    <h2>9. Критические ошибки (браковка поставки)</h2>
    <div class="critical">
        <p><strong>Приёмка немедленно останавливается и акт не подписывается при обнаружении любого из следующих фактов:</strong></p>
        <ul>
            <li><strong>Socket вместо RDMA</strong> — в логах NCCL указано <code>Using network: Socket</code> (а не IB/RoCE).</li>
            <li><strong>Отсутствие NVLink</strong> — топология показывает, что GPU общаются через CPU.</li>
            <li><strong>CUDA Python не установлен</strong> — <code>ImportError: No module named cuda</code>.</li>
            <li><strong>DDP падает с NCCL error</strong> — любая ошибка <code>NCCL timeout</code> или <code>unhandled system error</code>.</li>
            <li><strong>Illegal memory access</strong> — ошибка CUDA при работе DDP.</li>
            <li><strong>Нет поддержки INT8/INT4</strong> — аппаратное или программное отсутствие.</li>
        </ul>
    </div>

    <!-- 10. БОНУС-ТЕСТ -->
    <h2>10. Дополнительный бонус-тест (по желанию)</h2>
    <p>Запуск распределённой тренировки GPT-2 (124M параметров) через DDP с градиентной аккумуляцией:</p>
    <ul>
        <li>Использование всей VRAM обоих GPU.</li>
        <li><code>nvidia-smi</code> показывает 100% загрузки обоих GPU.</li>
        <li>Потери (loss) сходятся.</li>
    </ul>

    <!-- 11. ПОДПИСИ -->
    <h2>11. Подписи сторон</h2>
    <div class="signatures">
        <div class="signature-block">
            <p><strong>Заказчик</strong></p>
            <p>ФИО: _________________________</p>
            <p>Должность: ____________________</p>
            <div class="signature-line"></div>
            <p>Подпись: ______________________</p>
            <p>Дата: «___» __________ 2026 г.</p>
        </div>
        <div class="signature-block">
            <p><strong>Поставщик</strong></p>
            <p>ФИО: _________________________</p>
            <p>Должность: ____________________</p>
            <div class="signature-line"></div>
            <p>Подпись: ______________________</p>
            <p>Дата: «___» __________ 2026 г.</p>
        </div>
    </div>

    <div class="footer-note">
        Конец документа · Версия 1.0 · Все требования обязательны к исполнению
    </div>

</div>
</body>
</html>