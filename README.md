# asdfghjkl.github.io
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>李明 - 产品设计师</title>
    <!-- 引入外部资源 -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <!-- 配置Tailwind自定义主题 -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#3B82F6', // 主色调：蓝色
                        secondary: '#10B981', // 辅助色：绿色
                        dark: '#1F2937', // 深色
                        light: '#F9FAFB', // 浅色
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <!-- 自定义工具类 -->
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.1);
            }
            .transition-custom {
                transition: all 0.3s ease;
            }
        }
    </style>
    <style>
        /* 基础动画定义 */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .animate-fade-in {
            animation: fadeIn 0.8s ease forwards;
        }
        .delay-100 { animation-delay: 0.1s; }
        .delay-200 { animation-delay: 0.2s; }
        .delay-300 { animation-delay: 0.3s; }
        
        /* 滚动平滑效果 */
        html {
            scroll-behavior: smooth;
        }
        
        /* 导航栏滚动效果 */
        .navbar-scrolled {
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body class="font-sans text-dark bg-light">
    <!-- 导航栏 -->
    <nav id="navbar" class="fixed w-full z-50 transition-custom py-4">
        <div class="container mx-auto px-4 md:px-6 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-primary">李明</a>
            
            <!-- 桌面端导航 -->
            <div class="hidden md:flex items-center space-x-8">
                <a href="#home" class="font-medium hover:text-primary transition-custom">首页</a>
                <a href="#about" class="font-medium hover:text-primary transition-custom">关于我</a>
                <a href="#skills" class="font-medium hover:text-primary transition-custom">技能</a>
                <a href="#projects" class="font-medium hover:text-primary transition-custom">项目</a>
                <a href="#contact" class="font-medium hover:text-primary transition-custom">联系我</a>
                <a href="#" class="bg-primary text-white px-5 py-2 rounded-full hover:bg-primary/90 transition-custom">下载简历</a>
            </div>
            
            <!-- 移动端菜单按钮 -->
            <button id="menuBtn" class="md:hidden text-dark text-2xl">
                <<i class="fa fa-bars"></</i>
            </button>
        </div>
        
        <!-- 移动端导航菜单 -->
        <div id="mobileMenu" class="md:hidden hidden bg-white shadow-lg absolute w-full">
            <div class="container mx-auto px-4 py-4 flex flex-col space-y-4">
                <a href="#home" class="font-medium hover:text-primary transition-custom py-2 border-b border-gray-100">首页</a>
                <a href="#about" class="font-medium hover:text-primary transition-custom py-2 border-b border-gray-100">关于我</a>
                <a href="#skills" class="font-medium hover:text-primary transition-custom py-2 border-b border-gray-100">技能</a>
                <a href="#projects" class="font-medium hover:text-primary transition-custom py-2 border-b border-gray-100">项目</a>
                <a href="#contact" class="font-medium hover:text-primary transition-custom py-2 border-b border-gray-100">联系我</a>
                <a href="#" class="bg-primary text-white px-5 py-3 rounded-full hover:bg-primary/90 transition-custom text-center">下载简历</a>
            </div>
        </div>
    </nav>

    <!-- 英雄区 -->
    <section id="home" class="pt-32 pb-20 md:pt-40 md:pb-28 bg-gradient-to-br from-blue-50 to-indigo-50">
        <div class="container mx-auto px-4 md:px-6">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 animate-fade-in">
                    <h1 class="text-[clamp(2.5rem,5vw,4rem)] font-bold leading-tight text-dark mb-4">
                        专注于 <span class="text-primary">产品设计</span> 与 <span class="text-primary">用户体验</span>
                    </h1>
                    <p class="text-lg md:text-xl text-gray-600 mb-8 max-w-lg">
                        5年+产品设计经验，擅长将复杂问题简单化，创造直观、优雅且实用的数字产品体验
                    </p>
                    <div class="flex flex-col sm:flex-row gap-4">
                        <a href="#projects" class="bg-primary text-white px-8 py-3 rounded-full text-lg font-medium hover:bg-primary/90 transition-custom shadow-lg hover:shadow-xl">
                            查看作品集
                        </a>
                        <a href="#contact" class="bg-white text-primary border-2 border-primary px-8 py-3 rounded-full text-lg font-medium hover:bg-primary/5 transition-custom">
                            联系我
                        </a>
                    </div>
                    <div class="mt-10 flex space-x-6">
                        <a href="#" class="text-gray-500 hover:text-primary text-2xl transition-custom">
                            <<i class="fa fa-behance"></</i>
                        </a>
                        <a href="#" class="text-gray-500 hover:text-primary text-2xl transition-custom">
                            <<i class="fa fa-dribbble"></</i>
                        </a>
                        <a href="#" class="text-gray-500 hover:text-primary text-2xl transition-custom">
                            <<i class="fa fa-linkedin"></</i>
                        </a>
                        <a href="#" class="text-gray-500 hover:text-primary text-2xl transition-custom">
                            <<i class="fa fa-github"></</i>
                        </a>
                    </div>
                </div>
                <div class="md:w-1/2 mt-12 md:mt-0 animate-fade-in delay-200">
                    <div class="relative">
                        <div class="absolute -inset-4 bg-gradient-to-r from-primary to-secondary rounded-2xl blur-lg opacity-20"></div>
                        <img src="https://picsum.photos/id/1005/600/400" alt="产品设计师工作照" class="relative rounded-2xl shadow-2xl w-full object-cover h-[400px]">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 关于我 -->
    <section id="about" class="py-20 bg-white">
        <div class="container mx-auto px-4 md:px-6">
            <div class="text-center mb-16 animate-fade-in">
                <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold text-dark mb-4">关于我</h2>
                <div class="w-20 h-1 bg-primary mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-2xl mx-auto">专注产品设计领域5年，热衷于创造既美观又实用的数字产品</p>
            </div>
            
            <div class="flex flex-col md:flex-row gap-12 items-center">
                <div class="md:w-1/3 animate-fade-in delay-100">
                    <div class="relative">
                        <div class="absolute -inset-4 bg-gradient-to-r from-secondary to-primary rounded-2xl blur-lg opacity-20"></div>
                        <img src="https://picsum.photos/id/1012/400/500" alt="个人照片" class="relative rounded-2xl shadow-xl w-full object-cover h-[500px]">
                    </div>
                </div>
                
                <div class="md:w-2/3 animate-fade-in delay-200">
                    <h3 class="text-2xl font-bold mb-4">李明 | 产品设计师</h3>
                    <p class="text-gray-600 mb-6 leading-relaxed">
                        毕业于中央美术学院视觉传达设计专业，拥有5年互联网产品设计经验，曾任职于字节跳动、腾讯等知名企业，参与多个千万级用户产品的设计工作。
                    </p>
                    <p class="text-gray-600 mb-8 leading-relaxed">
                        我的设计理念是"以用户为中心，平衡美学与功能"，擅长用户研究、交互设计、视觉设计及产品思维，能够从0到1主导产品设计全流程，也能与开发、产品团队高效协作，推动设计落地。
                    </p>
                    
                    <div class="grid grid-cols-2 md:grid-cols-4 gap-6 mb-8">
                        <div class="text-center">
                            <div class="text-4xl font-bold text-primary mb-2">5+</div>
                            <p class="text-gray-600">工作年限</p>
                        </div>
                        <div class="text-center">
                            <div class="text-4xl font-bold text-primary mb-2">30+</div>
                            <p class="text-gray-600">完成项目</p>
                        </div>
                        <div class="text-center">
                            <div class="text-4xl font-bold text-primary mb-2">15+</div>
                            <p class="text-gray-600">合作客户</p>
                        </div>
                        <div class="text-center">
                            <div class="text-4xl font-bold text-primary mb-2">8+</div>
                            <p class="text-gray-600">设计奖项</p>
                        </div>
                    </div>
                    
                    <div class="flex flex-wrap gap-4">
                        <span class="bg-blue-100 text-primary px-4 py-2 rounded-full text-sm">UI/UX设计</span>
                        <span class="bg-green-100 text-secondary px-4 py-2 rounded-full text-sm">产品思维</span>
                        <span class="bg-purple-100 text-purple-600 px-4 py-2 rounded-full text-sm">用户研究</span>
                        <span class="bg-yellow-100 text-yellow-600 px-4 py-2 rounded-full text-sm">交互设计</span>
                        <span class="bg-red-100 text-red-600 px-4 py-2 rounded-full text-sm">视觉设计</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 技能展示 -->
    <section id="skills" class="py-20 bg-gray-50">
        <div class="container mx-auto px-4 md:px-6">
            <div class="text-center mb-16 animate-fade-in">
                <h2 class="text-[clamp(1.8rem,3vw,2.5rem)] font-bold text-dark mb-4">我的技能</h2>
                <div class="w-20 h-1 bg-primary mx-auto mb-6"></div>
                <p class="text-gray-600 max-w-2xl mx-auto">不断学习和提升，掌握设计全流程所需的核心技能</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- 技能卡片1 -->
                <div class="bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-custom animate-fade-in">
                    <div class="w-16 h-16 bg-blue-100 text-primary rounded-full flex items-center justify-center text-2xl mb-6">
                        <<i class="fa fa-paint-brush"></</i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">视觉设计</h3>
                    <p class="text-gray-600 mb-6">精通界面视觉设计，擅长色彩搭配、排版布局和动效设计，打造符合品牌调性的视觉体验</p>
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">Figma</span>
                                <span>95%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="bg-primary h-2.5 rounded-full" style="width: 95%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">Adobe XD</span>
                                <span>90%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="bg-primary h-2.5 rounded-full" style="width: 90%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">Photoshop</span>
                                <span>85%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="bg-primary h-2.5 rounded-full" style="width: 85%"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- 技能卡片2 -->
                <div class="bg-white rounded-2xl shadow-lg p-8 hover:shadow-xl transition-custom animate-fade-in delay-100">
                    <div class="w-16 h-16 bg-green-100 text-secondary rounded-full flex items-center justify-center text-2xl mb-6">
                        <<i class="fa fa-code-fork"></</i>
                    </div>
                    <h3 class="text-xl font-bold mb-4">交互设计</h3>
                    <p class="text-gray-600 mb-6">深入理解用户行为，设计直观、流畅的交互流程，提升产品易用性和用户满意度</p>
                    <div class="space-y-4">
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">用户流程图</span>
                                <span>92%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="bg-secondary h-2.5 rounded-full" style="width: 92%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">原型设计</span>
                                <span>96%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="bg-secondary h-2.5 rounded-full" style="width: 96%"></div>
                            </div>
                        </div>
                        <div>
                            <div class="flex justify-between mb-2">
                                <span class="font-medium">用户测试</span>
                                <span>88%</span>
                            </div>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="bg-secondary h-2.5 rounded-full" style="width: 88%"></div>
                            </div>