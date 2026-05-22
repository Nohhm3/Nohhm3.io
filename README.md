<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2026 AI/SW Career Portfolio</title>
    <!-- 외부 폰트: 프리텐다드 -->
    <link href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.8/dist/web/static/pretendard.css" rel="stylesheet">
    <style>
        /* CSS 변수 설정: 화이트 모드(기본) */
        :root {
            --bg-main: #ffffff;
            --bg-card: #f8f9fa;
            --text-main: #111111;
            --text-sub: #444444;
            --nav-bg: rgba(255, 255, 255, 0.85);
            --primary-navy: #0A192F;
            --point-blue: #007BFF;
            --neon-sky: #00F2FF;
            --border-color: #e9ecef;
            --timeline-line: #0A192F;
        }

        /* 다크 모드 설정 */
        body.dark-mode {
            --bg-main: #0b0e14;
            --bg-card: #1a1f26;
            --text-main: #f1f1f1;
            --text-sub: #cccccc;
            --nav-bg: rgba(11, 14, 20, 0.85);
            --primary-navy: #00F2FF;
            --point-blue: #4dabf7;
            --border-color: #2d343e;
            --timeline-line: #00F2FF;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Pretendard', sans-serif; }
        html { scroll-behavior: smooth; }
        body { background-color: var(--bg-main); color: var(--text-main); transition: 0.3s; line-height: 1.6; }

        /* Navigation */
        nav {
            position: fixed; top: 0; width: 100%; height: 70px;
            background-color: var(--nav-bg); backdrop-filter: blur(10px);
            display: flex; justify-content: space-between; align-items: center;
            padding: 0 5%; z-index: 1000; border-bottom: 1px solid var(--border-color);
        }
        .logo { font-weight: 800; font-size: 1.2rem; color: var(--point-blue); letter-spacing: -0.5px; }
        .nav-right { display: flex; align-items: center; gap: 25px; }
        .nav-links { display: flex; list-style: none; gap: 20px; }
        .nav-links a { text-decoration: none; color: var(--text-main); font-weight: 600; font-size: 0.9rem; transition: 0.2s; }
        .nav-links a:hover { color: var(--point-blue); }
        
        #theme-toggle {
            background: var(--text-main); color: var(--bg-main);
            border: none; padding: 7px 14px; border-radius: 20px;
            cursor: pointer; font-size: 0.75rem; font-weight: 700; transition: 0.3s;
        }

        /* Hero */
        .hero {
            height: 50vh; display: flex; flex-direction: column;
            justify-content: center; align-items: center; text-align: center;
            background: linear-gradient(180deg, var(--bg-card) 0%, var(--bg-main) 100%);
            padding: 0 20px; margin-top: 70px;
        }
        .hero h1 { font-size: 2.8rem; font-weight: 800; margin-bottom: 15px; letter-spacing: -1px; }
        .hero p { color: var(--point-blue); font-weight: 600; font-size: 1.1rem; }

        /* Content Sections */
        .container { max-width: 1000px; margin: 0 auto; padding: 40px 5% 100px; }
        .section-header { margin: 80px 0 40px; }
        .section-header h2 { font-size: 2rem; border-left: 6px solid var(--neon-sky); padding-left: 15px; }

        /* Cards */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 25px; }
        .card { 
            background: var(--bg-card); padding: 35px; border-radius: 20px; 
            border: 1px solid var(--border-color); transition: 0.3s;
        }
        .card:hover { transform: translateY(-8px); box-shadow: 0 15px 30px rgba(0,0,0,0.1); border-color: var(--point-blue); }
        .card h3 { color: var(--point-blue); margin-bottom: 15px; font-size: 1.25rem; }
        .card p { font-size: 0.95rem; color: var(--text-sub); }

        /* Vertical Timeline & Checklist */
        .timeline { position: relative; padding-left: 40px; }
        .timeline::before {
            content: ''; position: absolute; left: 10px; top: 0;
            width: 2px; height: 100%; background: var(--timeline-line); opacity: 0.3;
        }
        .timeline-item { position: relative; margin-bottom: 50px; }
        .timeline-dot {
            position: absolute; left: -36px; top: 5px;
            width: 14px; height: 14px; background: var(--neon-sky);
            border: 3px solid var(--timeline-line); border-radius: 50%;
        }
        .year-title { font-weight: 800; font-size: 1.3rem; color: var(--text-main); margin-bottom: 15px; display: block; }
        
        .checklist-card { background: var(--bg-card); padding: 25px; border-radius: 15px; border: 1px solid var(--border-color); }
        .checklist-card h4 { font-size: 1rem; margin-bottom: 15px; color: var(--point-blue); }
        .checklist { list-style: none; }
        .checklist li { margin-bottom: 12px; display: flex; align-items: flex-start; gap: 12px; font-size: 0.95rem; cursor: pointer; }
        .checklist input[type="checkbox"] {
            width: 20px; height: 20px; accent-color: var(--neon-sky); cursor: pointer; margin-top: 2px;
        }
        .checklist input:checked + span { text-decoration: line-through; opacity: 0.5; }

        footer { text-align: center; padding: 60px; border-top: 1px solid var(--border-color); opacity: 0.6; font-size: 0.85rem; }

        /* Mobile Responsive */
        @media (max-width: 768px) {
            .nav-links { display: none; }
            .hero h1 { font-size: 2rem; }
            .section-header h2 { font-size: 1.6rem; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">PORTFOLIO 2026</div>
        <div class="nav-right">
            <ul class="nav-links">
                <li><a href="#jobs">미래 직무</a></li>
                <li><a href="#skills">핵심 역량</a></li>
                <li><a href="#roadmap">로드맵</a></li>
            </ul>
            <button id="theme-toggle" onclick="toggleTheme()">DARK MODE</button>
        </div>
    </nav>

    <header class="hero">
        <h1>나만의 AI/SW 진로 분석</h1>
        <p>2026 IT 블루오션 직무 및 커리어 로드맵 전략</p>
    </header>

    <div class="container">
        <!-- Section 1: Jobs -->
        <section id="jobs">
            <div class="section-header">
                <h2>미래 유망 직무</h2>
            </div>
            <div class="grid">
                <div class="card">
                    <h3>AI 엔지니어링 및 ModelOps 전문가</h3>
                    <p>AI 모델의 배포, 모니터링, 재사용 가능한 파이프라인을 구축하는 직무로, 현재 공급이 극히 적은 블루오션 인력입니다 [1].</p>
                </div>
                <div class="card">
                    <h3>AI TRiSM 및 거버넌스 해석가</h3>
                    <p>AI의 편향성 및 리스크를 관리하며, 이를 비즈니스 언어로 번역하고 운영 단계에서 통합 관리하는 전문가입니다 [2].</p>
                </div>
                <div class="card">
                    <h3>멀티 에이전트 오케스트레이터</h3>
                    <p>여러 AI 에이전트 간의 상호작용을 설계하고 비즈니스 로직에 맞게 지휘하는 고난도·고부가가치 직무입니다 [3].</p>
                </div>
            </div>
        </section>

        <!-- Section 2: Skills -->
        <section id="skills">
            <div class="section-header">
                <h2>핵심 필수 역량</h2>
            </div>
            <div class="grid">
                <div class="card">
                    <h3>거버넌스 해석 (Governance)</h3>
                    <p>기술적 리스크를 비즈니스 언어로 번역하고, 리스크 관리 프레임워크를 개발 표준으로 변환하는 능력입니다 [4].</p>
                </div>
                <div class="card">
                    <h3>시스템 합성 및 오케스트레이션</h3>
                    <p>전체 시스템 아키텍처를 조합하고 여러 AI 에이전트 간의 협업 워크플로우를 지휘하는 설계 역량입니다 [5].</p>
                </div>
                <div class="card">
                    <h3>데이터 옵저버빌리티</h3>
                    <p>데이터 품질을 실시간 감시하고 AI 학습 적합성을 판별하여 파이프라인 병목 현상을 해결하는 핵심 역량입니다 [5].</p>
                </div>
            </div>
        </section>

        <!-- Section 3: Roadmap -->
        <section id="roadmap">
            <div class="section-header">
                <h2>나의 4년 로드맵</h2>
            </div>
            <div class="timeline">
                <!-- 1학년 -->
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <span class="year-title">1학년: AI 네이티브 기초</span>
                    <div class="checklist-card">
                        <h4>학습 목표: CS 기초 및 AI 도구 숙달 [6]</h4>
                        <ul class="checklist">
                            <li><label><input type="checkbox"> <span>Claude, Cursor 등 AI 에이전트 활용 코딩 습득</span></label></li>
                            <li><label><input type="checkbox"> <span>자료구조, 알고리즘, Git 기반 협업 기초 확립</span></label></li>
                        </ul>
                    </div>
                </div>
                <!-- 2학년 -->
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <span class="year-title">2학년: 백엔드 및 인프라 구축</span>
                    <div class="checklist-card">
                        <h4>학습 목표: 서버 아키텍처 및 데이터 이해 [7]</h4>
                        <ul class="checklist">
                            <li><label><input type="checkbox"> <span>Spring Framework 및 RESTful API 설계 역량 확보</span></label></li>
                            <li><label><input type="checkbox"> <span>MySQL 및 Kafka 등 대용량 데이터 처리 기초 습득</span></label></li>
                            <li><label><input type="checkbox"> <span>Docker를 활용한 컨테이너화 기술 습득</span></label></li>
                        </ul>
                    </div>
                </div>
                <!-- 3학년 -->
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <span class="year-title">3학년: ModelOps 고도화</span>
                    <div class="checklist-card">
                        <h4>학습 목표: AI 모델 운영 및 클라우드 실습 [7]</h4>
                        <ul class="checklist">
                            <li><label><input type="checkbox"> <span>AI 모델 버전 관리 및 ModelOps 플랫폼 이해</span></label></li>
                            <li><label><input type="checkbox"> <span>AWS/GCP 환경에서 CI/CD 및 모니터링 시스템 구축</span></label></li>
                        </ul>
                    </div>
                </div>
                <!-- 4학년 -->
                <div class="timeline-item">
                    <div class="timeline-dot"></div>
                    <span class="year-title">4학년: 거버넌스 및 멀티 에이전트</span>
                    <div class="checklist-card">
                        <h4>학습 목표: 리스크 통제 및 복합 서비스 완성 [8]</h4>
                        <ul class="checklist">
                            <li><label><input type="checkbox"> <span>AI TRiSM 기반 거버넌스 프레임워크 구현 프로젝트</span></label></li>
                            <li><label><input type="checkbox"> <span>멀티 에이전트 오케스트레이션 기반 캡스톤 프로젝트</span></label></li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2024 AI/SW Career Roadmap Portfolio. 분석 데이터: 2026 전략 기술 트렌드 리포트 기반.</p>
    </footer>

    <script>
        // 테마 전환 함수
        function toggleTheme() {
            const body = document.body;
            const btn = document.getElementById('theme-toggle');
            
            body.classList.toggle('dark-mode');
            
            if(body.classList.contains('dark-mode')) {
                btn.textContent = 'LIGHT MODE';
                localStorage.setItem('theme', 'dark');
            } else {
                btn.textContent = 'DARK MODE';
                localStorage.setItem('theme', 'light');
            }
        }

        // 로컬 스토리지에 테마 설정 저장 (새로고침해도 유지)
        window.onload = () => {
            if(localStorage.getItem('theme') === 'dark') {
                document.body.classList.add('dark-mode');
                document.getElementById('theme-toggle').textContent = 'LIGHT MODE';
            }
        };

        // 체크박스 상태 저장 (선택 사항)
        const checkboxes = document.querySelectorAll('input[type="checkbox"]');
        checkboxes.forEach((cb, index) => {
            const savedStatus = localStorage.getItem('step-' + index);
            if(savedStatus === 'true') cb.checked = true;

            cb.addEventListener('change', () => {
                localStorage.setItem('step-' + index, cb.checked);
            });
        });
    </script>
</body>
</html>
