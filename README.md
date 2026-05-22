<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2026 AI/SW Career Portfolio</title>
    <link href="https://fonts.googleapis.com/css2?family=Pretendard:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
        /* 변수 설정: 화이트 모드(기본) */
        :root {
            --bg-color: #ffffff;
            --text-color: #111111;
            --nav-bg: rgba(255, 255, 255, 0.8);
            --card-bg: #f8f9fa;
            --primary-navy: #0A192F;
            --point-blue: #007BFF;
            --neon-sky: #00F2FF;
            --border-color: #eeeeee;
        }

        /* 다크 모드 설정 */
        body.dark-mode {
            --bg-color: #0b0e14;
            --text-color: #e0e0e0;
            --nav-bg: rgba(11, 14, 20, 0.8);
            --card-bg: #1a1f26;
            --primary-navy: #00F2FF; /* 다크모드에선 포인트 컬러 강조 */
            --point-blue: #4dabf7;
            --border-color: #2d343e;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Pretendard', sans-serif; }
        html { scroll-behavior: smooth; }
        body { background-color: var(--bg-color); color: var(--text-color); transition: background 0.3s, color 0.3s; line-height: 1.6; }

        /* Navigation */
        nav {
            position: fixed; top: 0; width: 100%; height: 70px;
            background-color: var(--nav-bg); backdrop-filter: blur(10px);
            display: flex; justify-content: space-between; align-items: center;
            padding: 0 5%; z-index: 1000; border-bottom: 1px solid var(--border-color);
        }
        .logo { font-weight: 800; font-size: 1.2rem; color: var(--point-blue); }
        .nav-right { display: flex; align-items: center; gap: 20px; }
        .nav-links { display: flex; list-style: none; gap: 20px; }
        .nav-links a { text-decoration: none; color: var(--text-color); font-weight: 600; font-size: 0.9rem; }
        
        /* Theme Toggle Button */
        #theme-toggle {
            background: var(--text-color); color: var(--bg-color);
            border: none; padding: 8px 15px; border-radius: 20px;
            cursor: pointer; font-size: 0.8rem; font-weight: 600;
        }

        /* Sections */
        .container { max-width: 1000px; margin: 0 auto; padding: 100px 5% 50px; }
        header { text-align: center; margin-bottom: 80px; }
        header h1 { font-size: 2.5rem; margin-bottom: 15px; color: var(--text-color); }
        header p { color: var(--point-blue); font-weight: 600; }

        .section-title { font-size: 1.8rem; margin: 60px 0 30px; border-left: 5px solid var(--neon-sky); padding-left: 15px; }

        /* Grid Cards */
        .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
        .card { background: var(--card-bg); padding: 30px; border-radius: 15px; border: 1px solid var(--border-color); }
        .card h3 { color: var(--point-blue); margin-bottom: 15px; }
        .card p { font-size: 0.95rem; opacity: 0.9; }

        /* Vertical Timeline with Checklist */
        .timeline { position: relative; padding-left: 30px; border-left: 2px solid var(--border-color); margin-left: 10px; }
        .timeline-item { position: relative; margin-bottom: 40px; }
        .timeline-item::before {
            content: ''; position: absolute; left: -41px; top: 5px;
            width: 20px; height: 20px; background: var(--bg-color);
            border: 4px solid var(--neon-sky); border-radius: 50%;
        }
        .year-label { font-weight: 800; font-size: 1.2rem; color: var(--point-blue); margin-bottom: 10px; display: block; }
        .roadmap-card { background: var(--card-bg); padding: 20px; border-radius: 12px; }
        
        .checklist { list-style: none; margin-top: 10px; }
        .checklist li { margin-bottom: 10px; display: flex; align-items: flex-start; gap: 10px; font-size: 0.95rem; }
        .checklist input[type="checkbox"] {
            margin-top: 5px; width: 18px; height: 18px; cursor: pointer;
            accent-color: var(--neon-sky);
        }
        .checklist input[type="checkbox"]:checked + span { text-decoration: line-through; opacity: 0.5; }

        footer { text-align: center; padding: 50px; opacity: 0.6; font-size: 0.8rem; border-top: 1px solid var(--border-color); }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-links { display: none; }
            header h1 { font-size: 1.8rem; }
        }
    </style>
</head>
<body>

    <nav>
        <div class="logo">2026 AI/SW CAREER</div>
        <div class="nav-right">
            <ul class="nav-links">
                <li><a href="#jobs">미래 직무</a></li>
                <li><a href="#skills">핵심 역량</a></li>
                <li><a href="#roadmap">로드맵</a></li>
            </ul>
            <button id="theme-toggle">다크 모드</button>
        </div>
    </nav>

    <div class="container">
        <header>
            <h1>나만의 AI/SW 진로 분석 포트폴리오</h1>
            <p>기술 트렌드 분석을 통한 2026 커리어 전략</p>
        </header>

        <!-- Section 1: Future Jobs -->
        <section id="jobs">
            <h2 class="section-title">미래 유망 직무 (Blue Ocean)</h2>
            <div class="grid">
                <div class="card">
                    <h3>AI 엔지니어링 및 ModelOps</h3>
                    <p>AI 모델의 배포, 모니터링, 재사용 가능한 파이프라인을 구축하는 전문가로 현재 공급이 극히 적은 블루오션 인력입니다 [1].</p>
                </div>
                <div class="card">
                    <h3>AI TRiSM 및 거버넌스 해석가</h3>
                    <p>AI의 편향성 및 환각 현상 리스크를 관리하며, 이를 비즈니스 언어로 번역하여 운영 단계에서 통합 관리합니다 [2, 3].</p>
                </div>
                <div class="card">
                    <h3>멀티 에이전트 오케스트레이터</h3>
                    <p>복잡한 업무를 수행하는 여러 AI 에이전트 간의 상호작용을 설계하고 비즈니스 로직에 맞게 지휘하는 고부가가치 직무입니다 [2].</p>
                </div>
            </div>
        </section>

        <!-- Section 2: Core Skills -->
        <section id="skills">
            <h2 class="section-title">대체 불가능 핵심 역량</h2>
            <div class="grid">
                <div class="card">
                    <h3>거버넌스 해석</h3>
                    <p>기술적 리스크를 비즈니스 언어로 번역하고 리스크 관리 프레임워크를 개발 표준으로 변환하는 능력입니다 [3].</p>
                </div>
                <div class="card">
                    <h3>시스템 합성 및 오케스트레이션</h3>
                    <p>개별 코드를 쓰는 것보다 전체 시스템 아키텍처를 조합하고 AI 에이전트 간의 협업 워크플로우를 설계하는 역량입니다 [4].</p>
                </div>
                <div class="card">
                    <h3>데이터 옵저버빌리티</h3>
                    <p>데이터 품질을 실시간 감시하고 AI 학습 적합성을 판별하여 파이프라인의 병목 현상을 해결하는 핵심 역량입니다 [4].</p>
                </div>
            </div>
        </section>

        <!-- Section 3: Roadmap (Timeline & Checklist) -->
        <section id="roadmap">
            <h2 class="section-title">나의 4년 커리어 로드맵</h2>
            <div class="timeline">
                <!-- 1학년 -->
                <div class="timeline-item">
                    <span class="year-label">1학년: AI 네이티브 기초</span>
                    <div class="roadmap-card">
                        <ul class="checklist">
                            <li><input type="checkbox"> <span>Claude, Cursor 등 AI 에이전트 활용 코딩 습득 [2]</span></li>
                            <li><input type="checkbox"> <span>자료구조, 알고리즘 등 CS 기본기 다지기</span></li>
                        </ul>
                    </div>
                </div>
                <!-- 2학년 -->
                <div class="timeline-item">
                    <span class="year-label">2학년: 백엔드 및 데이터 인프라</span>
                    <div class="roadmap-card">
                        <ul class="checklist">
                            <li><input type="checkbox"> <span>Spring Framework 및 RESTful API 설계 역량 확보 [5]</span></li>
                            <li><input type="checkbox"> <span>MySQL 모델링 및 Kafka 등 대용량 데이터 처리 기초 습득 [5]</span></li>
                            <li><input type="checkbox"> <span>Docker를 활용한 컨테이너화 기술 입문 [5]</span></li>
                        </ul>
                    </div>
                </div>
                <!-- 3학년 -->
                <div class="timeline-item">
                    <span class="year-label">3학년: ModelOps 및 클라우드 고도화</span>
                    <div class="roadmap-card">
                        <ul class="checklist">
                            <li><input type="checkbox"> <span>AI 모델 버전 관리 및 ModelOps 플랫폼 구축 실습 [5]</span></li>
                            <li><input type="checkbox"> <span>AWS/GCP 환경에서 CI/CD 및 모니터링 시스템 구축 [5]</span></li>
                            <li><input type="checkbox"> <span>클라우드 기반 AI 모델 서빙 및 자동 재학습 시스템 프로젝트 [5]</span></li>
                        </ul>
                    </div>
                </div>
                <!-- 4학년 -->
                <div class="timeline-item">
                    <span class="year-label">4학년: 시스템 설계 및 리스크 관리</span>
                    <div class="roadmap-card">
                        <ul class="checklist">
                            <li><input type="checkbox"> <span>AI TRiSM 체계 내 리스크 관리 및 거버넌스 프로젝트 [3]</span></li>
                            <li><input type="checkbox"> <span>멀티 에이전트 오케스트레이션 기반 비즈니스 서비스 설계 [4]</span></li>
                            <li><input type="checkbox"> <span>실무형 캡스톤 디자인 및 포트폴리오 완성</span></li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2024 AI/SW Career Portfolio. 분석 데이터 출처: 2026 IT 블루오션 직무 분석 리포트 및 전략 기술 트렌드.</p>
    </footer>

    <script>
        // 다크 모드 토글 로직
        const themeToggle = document.getElementById('theme-toggle');
        const body = document.body;

        themeToggle.addEventListener('click', () => {
            body.classList.toggle('dark-mode');
            if (body.classList.contains('dark-mode')) {
                themeToggle.textContent = '화이트 모드';
            } else {
                themeToggle.textContent = '다크 모드';
            }
        });

        // 네비게이션 부드러운 스크롤 (이미 CSS smooth scroll이 적용되어 있으나 호환성을 위해 유지)
        document.querySelectorAll('nav a').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('href');
                document.querySelector(targetId).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
