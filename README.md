<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>昆仑F5 | 摄影作品分享平台 - kunlunF5.com</title>
    <!-- Tailwind CSS v3 国内加速CDN -->
    <script src="https://cdn.bootcdn.net/ajax/libs/tailwindcss/3.3.5/tailwind.min.js"></script>
    <!-- Font Awesome 国内加速CDN -->
    <link href="https://cdn.bootcdn.net/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <!-- 统一的 Tailwind 配置【修复核心错误：darkMode改为根级别】 -->
    <script>
        tailwind.config = {
            darkMode: 'class', // 修复：移到根级别，正确生效
            theme: {
                extend: {
                    colors: {
                        primary: '#2d3748',      // 深灰色
                        secondary: '#4a5568',    // 中灰色
                        accent: '#1a202c',       // 近黑色
                        light: '#f7fafc',        // 浅灰色
                        highlight: '#667eea',    // 蓝紫色
                    },
                    fontFamily: {
                        sans: ['Inter', 'system-ui', 'sans-serif'],
                        display: ['Playfair Display', 'serif'],
                    },
                    boxShadow: {
                        'card': '0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06)',
                        'card-hover': '0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05)',
                    },
                    animation: {
                        'fade-in': 'fadeIn 0.5s ease-in-out',
                        'slide-up': 'slideUp 0.5s ease-in-out',
                        'scale-in': 'scaleIn 0.3s ease-in-out', // 修复：补充缺失的动画
                    },
                    keyframes: {
                        fadeIn: {
                            '0%': { opacity: '0' },
                            '100%': { opacity: '1' },
                        },
                        slideUp: {
                            '0%': { transform: 'translateY(20px)', opacity: '0' },
                            '100%': { transform: 'translateY(0)', opacity: '1' },
                        },
                        scaleIn: { // 修复：补充scale-in动画的关键帧
                            '0%': { transform: 'scale(0.9)', opacity: '0' },
                            '100%': { transform: 'scale(1)', opacity: '1' },
                        }
                    },
                }
            }
        }
    </script>
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            }
            .text-shadow-lg {
                text-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            }
            .backdrop-blur {
                backdrop-filter: blur(8px);
            }
            .scrollbar-hide::-webkit-scrollbar {
                display: none;
            }
            .scrollbar-hide {
                -ms-overflow-style: none;
                scrollbar-width: none;
            }
            .hover-scale {
                @apply transition-transform duration-300 hover:scale-105;
            }
            .card-overlay {
                background: linear-gradient(to top, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0) 60%);
            }
            .video-indicator {
                @apply absolute top-3 right-3 bg-red-500 rounded-full w-3 h-3 animate-pulse;
            }
        }
    </style>
    <!-- 国内字体库 替换谷歌字体（修复加载超时） -->
    <link href="https://cdn.bootcdn.net/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
    <style>
        @import url('https://cdn.bootcdn.net/ajax/libs/inter-ui/3.19.3/inter.min.css');
        @import url('https://cdn.bootcdn.net/ajax/libs/playfair-display/2.301/playfair-display.min.css');
    </style>
    <!-- SEO Meta Tags 适配GitHub部署 -->
    <meta name="description" content="昆仑F5 - 专业摄影作品分享平台，邀请制高质量摄影社区">
    <meta name="keywords" content="摄影,摄影作品,摄影社区,邀请制,照片分享,视频分享,kunlunF5,昆仑F5">
    <meta name="author" content="昆仑F5团队">
    <meta name="robots" content="index, follow">
    <meta property="og:title" content="昆仑F5 | 摄影作品分享平台">
    <meta property="og:description" content="昆仑F5 - 专业摄影作品分享平台，邀请制高质量摄影社区">
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://kunlunF5.com">
    <meta property="og:image" content="https://p11-doubao-search-sign.byteimg.com/labis/7f1d85ddbf475fd67afce61368dfb04d~tplv-be4g95zd3a-image.jpeg">
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="昆仑F5 | 摄影作品分享平台">
    <meta name="twitter:description" content="昆仑F5 - 专业摄影作品分享平台，邀请制高质量摄影社区">
    <meta name="twitter:image" content="https://p11-doubao-search-sign.byteimg.com/labis/7f1d85ddbf475fd67afce61368dfb04d~tplv-be4g95zd3a-image.jpeg">
    <!-- 网站图标 -->
    <link rel="icon" href="https://p11-doubao-search-sign.byteimg.com/labis/7f1d85ddbf475fd67afce61368dfb04d~tplv-be4g95zd3a-image.jpeg" type="image/jpeg">
    <link rel="apple-touch-icon" href="https://p11-doubao-search-sign.byteimg.com/labis/7f1d85ddbf475fd67afce61368dfb04d~tplv-be4g95zd3a-image.jpeg">
</head>
<body class="bg-gray-100 dark:bg-gray-900 text-gray-800 dark:text-gray-200 min-h-screen flex flex-col">
    <!-- 导航栏 -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-white bg-opacity-90 dark:bg-gray-800 dark:bg-opacity-90 backdrop-blur shadow-sm">
        <div class="container mx-auto px-4 py-3 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <a href="#" class="text-2xl font-display font-bold text-primary dark:text-white">昆仑F5</a>
                <span class="hidden sm:inline-block text-xs bg-gray-200 dark:bg-gray-700 text-gray-600 dark:text-gray-300 px-2 py-1 rounded-full">邀请制</span>
            </div>
            
            <div class="hidden md:flex items-center space-x-8">
                <a href="#discover" class="text-gray-600 dark:text-gray-300 hover:text-primary dark:hover:text-white transition-colors">发现</a>
                <a href="#categories" class="text-gray-600 dark:text-gray-300 hover:text-primary dark:hover:text-white transition-colors">分类</a>
                <a href="#featured" class="text-gray-600 dark:text-gray-300 hover:text-primary dark:hover:text-white transition-colors">精选</a>
                <a href="#photographers" class="text-gray-600 dark:text-gray-300 hover:text-primary dark:hover:text-white transition-colors">摄影师</a>
            </div>
            
            <div class="flex items-center space-x-4">
                <button id="searchBtn" class="text-gray-600 dark:text-gray-300 hover:text-primary dark:hover:text-white transition-colors">
                    <i class="fa fa-search text-lg"></i>
                </button>
                <button id="themeToggleBtn" class="text-gray-600 dark:text-gray-300 hover:text-primary dark:hover:text-white transition-colors">
                    <i class="fa fa-moon-o dark:hidden text-lg"></i>
                    <i class="fa fa-sun-o hidden dark:block text-lg"></i>
                </button>
                <div class="relative">
                    <button id="userMenuBtn" class="flex items-center space-x-1 focus:outline-none">
                        <div class="w-8 h-8 rounded-full bg-gray-200 dark:bg-gray-700 flex items-center justify-center">
                            <i class="fa fa-user text-gray-500 dark:text-gray-400"></i>
                        </div>
                        <span class="hidden sm:block text-sm font-medium">登录</span>
                    </button>
                    <div id="userMenu" class="absolute right-0 mt-2 w-48 bg-white dark:bg-gray-800 rounded-lg shadow-lg py-1 z-10 hidden animate-fade-in">
                        <a href="#" id="loginBtn" class="block px-4 py-2 text-sm text-gray-700 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-700">
                            <i class="fa fa-sign-in mr-2"></i>登录
                        </a>
                        <a href="#" id="registerBtn" class="block px-4 py-2 text-sm text-gray-700 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-700">
                            <i class="fa fa-user-plus mr-2"></i>注册
                        </a>
                        <hr class="my-1 border-gray-200 dark:border-gray-700">
                        <a href="#" id="adminLoginBtn" class="block px-4 py-2 text-sm text-gray-700 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-700">
                            <i class="fa fa-lock mr-2"></i>管理员登录
                        </a>
                        <a href="#" id="userProfileBtn" class="block px-4 py-2 text-sm text-gray-700 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-700 hidden">
                            <i class="fa fa-user mr-2"></i>个人中心
                        </a>
                        <a href="#" id="uploadBtn" class="block px-4 py-2 text-sm text-gray-700 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-700 hidden">
                            <i class="fa fa-upload mr-2"></i>上传作品
                        </a>
                        <a href="#" id="logoutBtn" class="block px-4 py-2 text-sm text-gray-700 dark:text-gray-300 hover:bg-gray-100 dark:hover:bg-gray-700 hidden">
                            <i class="fa fa-sign-out mr-2"></i>退出登录
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <!-- 主要内容 -->
    <main class="flex-1 pt-16">
        <!-- 英雄区域 -->
        <section class="relative h-[80vh] min-h-[500px] flex items-center justify-center overflow-hidden">
            <div class="absolute inset-0 z-0">
                <img src="https://p11-doubao-search-sign.byteimg.com/labis/7f1d85ddbf475fd67afce61368dfb04d~tplv-be4g95zd3a-image.jpeg" alt="风景摄影" class="w-full h-full object-cover">
                <div class="absolute inset-0 bg-black bg-opacity-40"></div>
            </div>
            <div class="container mx-auto px-4 z-10 text-center">
                <h1 class="text-4xl md:text-6xl font-display font-bold text-white text-shadow-lg mb-4 animate-fade-in">
                    捕捉瞬间，<br class="md:hidden">定格永恒
                </h1>
                <p class="text-xl md:text-2xl text-gray-100 text-shadow mb-8 max-w-2xl mx-auto animate-slide-up">
                    加入我们的邀请制摄影社区，与全球摄影师分享你的视觉故事
                </p>
                <div class="flex flex-col sm:flex-row items-center justify-center space-y-4 sm:space-y-0 sm:space-x-4 animate-slide-up" style="animation-delay: 0.2s;">
                    <button id="getInviteBtn" class="px-8 py-3 bg-white text-gray-900 rounded-full font-medium hover:bg-gray-100 transition-colors shadow-lg">
                        获取邀请码
                    </button>
                    <button id="exploreBtn" class="px-8 py-3 bg-transparent border-2 border-white text-white rounded-full font-medium hover:bg-white hover:text-gray-900 transition-colors">
                        探索作品
                    </button>
                </div>
            </div>
            <div class="absolute bottom-8 left-0 right-0 flex justify-center animate-bounce">
                <a href="#discover" class="text-white">
                    <i class="fa fa-chevron-down text-2xl"></i>
                </a>
            </div>
        </section>

        <!-- 发现区域 -->
        <section id="discover" class="py-16 bg-white dark:bg-gray-800">
            <div class="container mx-auto px-4">
                <div class="flex flex-col md:flex-row items-start md:items-center justify-between mb-8">
                    <div>
                        <h2 class="text-3xl font-display font-bold mb-2">发现精彩</h2>
                        <p class="text-gray-600 dark:text-gray-400">探索最新上传的摄影作品和视频</p>
                    </div>
                    <div class="flex items-center space-x-2 mt-4 md:mt-0">
                        <button class="filter-btn active px-4 py-2 rounded-full bg-gray-100 dark:bg-gray-700 text-gray-800 dark:text-gray-200 hover:bg-gray-200 dark:hover:bg-gray-600 transition-colors" data-filter="all">
                            全部
                        </button>
                        <button class="filter-btn px-4 py-2 rounded-full text-gray-600 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 transition-colors" data-filter="photos">
                            照片
                        </button>
                        <button class="filter-btn px-4 py-2 rounded-full text-gray-600 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 transition-colors" data-filter="videos">
                            视频
                        </button>
                    </div>
                </div>

                <!-- 作品网格 -->
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
                    <div class="work-item photos group" data-category="landscape">
                        <div class="relative rounded-xl overflow-hidden shadow-card hover:shadow-card-hover transition-shadow duration-300">
                            <img src="https://p11-doubao-search-sign.byteimg.com/labis/7ad7772a72899c6d80dc75aa2406f158~tplv-be4g95zd3a-image.jpeg" alt="山水风景" class="w-full h-80 object-cover hover-scale">
                            <div class="absolute inset-0 card-overlay opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4">
                                <h3 class="text-white font-medium text-lg">山间倒影</h3>
                                <p class="text-gray-200 text-sm">美国怀俄明州</p>
                                <div class="flex items-center justify-between mt-3">
                                    <div class="flex items-center space-x-2">
                                        <div class="w-6 h-6 rounded-full bg-gray-300 flex items-center justify-center">
                                            <i class="fa fa-user text-xs text-gray-600"></i>
                                        </div>
                                        <span class="text-white text-xs">Alex Morgan</span>
                                    </div>
                                    <div class="flex items-center space-x-3">
                                        <button class="text-white hover:text-red-400 transition-colors">
                                            <i class="fa fa-heart-o"></i>
                                        </button>
                                        <button class="text-white hover:text-blue-400 transition-colors">
                                            <i class="fa fa-bookmark-o"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="work-item photos group" data-category="portrait">
                        <div class="relative rounded-xl overflow-hidden shadow-card hover:shadow-card-hover transition-shadow duration-300">
                            <img src="https://p3-doubao-search-sign.byteimg.com/labis/479287ac6bee78eaed2e3bc77b429759~tplv-be4g95zd3a-image.jpeg" alt="人像摄影" class="w-full h-80 object-cover hover-scale">
                            <div class="absolute inset-0 card-overlay opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4">
                                <h3 class="text-white font-medium text-lg">东方韵味</h3>
                                <p class="text-gray-200 text-sm">传统建筑人像</p>
                                <div class="flex items-center justify-between mt-3">
                                    <div class="flex items-center space-x-2">
                                        <div class="w-6 h-6 rounded-full bg-gray-300 flex items-center justify-center">
                                            <i class="fa fa-user text-xs text-gray-600"></i>
                                        </div>
                                        <span class="text-white text-xs">Li Wei</span>
                                    </div>
                                    <div class="flex items-center space-x-3">
                                        <button class="text-white hover:text-red-400 transition-colors">
                                            <i class="fa fa-heart-o"></i>
                                        </button>
                                        <button class="text-white hover:text-blue-400 transition-colors">
                                            <i class="fa fa-bookmark-o"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="work-item videos group" data-category="landscape">
                        <div class="relative rounded-xl overflow-hidden shadow-card hover:shadow-card-hover transition-shadow duration-300">
                            <img src="https://p11-doubao-search-sign.byteimg.com/labis/488900cb87c286be047c6cdf951a88ee~tplv-be4g95zd3a-image.jpeg" alt="延时摄影" class="w-full h-80 object-cover hover-scale">
                            <div class="video-indicator"></div>
                            <div class="absolute inset-0 flex items-center justify-center">
                                <div class="w-16 h-16 rounded-full bg-white bg-opacity-70 flex items-center justify-center hover:bg-opacity-90 transition-all duration-300 hover:scale-110 cursor-pointer">
                                    <i class="fa fa-play text-gray-900 text-xl"></i>
                                </div>
                            </div>
                            <div class="absolute inset-0 card-overlay opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4">
                                <h3 class="text-white font-medium text-lg">日落时分</h3>
                                <p class="text-gray-200 text-sm">延时摄影短片</p>
                                <div class="flex items-center justify-between mt-3">
                                    <div class="flex items-center space-x-2">
                                        <div class="w-6 h-6 rounded-full bg-gray-300 flex items-center justify-center">
                                            <i class="fa fa-user text-xs text-gray-600"></i>
                                        </div>
                                        <span class="text-white text-xs">David Chen</span>
                                    </div>
                                    <div class="flex items-center space-x-3">
                                        <button class="text-white hover:text-red-400 transition-colors">
                                            <i class="fa fa-heart-o"></i>
                                        </button>
                                        <button class="text-white hover:text-blue-400 transition-colors">
                                            <i class="fa fa-bookmark-o"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="work-item photos group" data-category="blackwhite">
                        <div class="relative rounded-xl overflow-hidden shadow-card hover:shadow-card-hover transition-shadow duration-300">
                            <img src="https://p3-doubao-search-sign.byteimg.com/labis/7ff49ae9b6c41ed1e201f1060c771c22~tplv-be4g95zd3a-image.jpeg" alt="黑白摄影" class="w-full h-80 object-cover hover-scale">
                            <div class="absolute inset-0 card-overlay opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4">
                                <h3 class="text-white font-medium text-lg">思绪</h3>
                                <p class="text-gray-200 text-sm">黑白人像摄影</p>
                                <div class="flex items-center justify-between mt-3">
                                    <div class="flex items-center space-x-2">
                                        <div class="w-6 h-6 rounded-full bg-gray-300 flex items-center justify-center">
                                            <i class="fa fa-user text-xs text-gray-600"></i>
                                        </div>
                                        <span class="text-white text-xs">Emma Zhang</span>
                                    </div>
                                    <div class="flex items-center space-x-3">
                                        <button class="text-white hover:text-red-400 transition-colors">
                                            <i class="fa fa-heart-o"></i>
                                        </button>
                                        <button class="text-white hover:text-blue-400 transition-colors">
                                            <i class="fa fa-bookmark-o"></i>
                                        </button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="mt-12 text-center">
                    <button id="loadMoreBtn" class="px-8 py-3 bg-gray-100 dark:bg-gray-700 text-gray-800 dark:text-gray-200 rounded-full font-medium hover:bg-gray-200 dark:hover:bg-gray-600 transition-colors">
                        加载更多
                    </button>
                </div>
            </div>
        </section>

        <!-- 分类区域 -->
        <section id="categories" class="py-16 bg-gray-50 dark:bg-gray-900">
            <div class="container mx-auto px-4">
                <div class="text-center mb-12">
                    <h2 class="text-3xl font-display font-bold mb-2">浏览分类</h2>
                    <p class="text-gray-600 dark:text-gray-400 max-w-2xl mx-auto">探索不同类型的摄影作品，发现你感兴趣的内容</p>
                </div>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-4">
                    <a href="#" class="category-item group">
                        <div class="relative rounded-xl overflow-hidden h-40">
                            <img src="https://p11-doubao-search-sign.byteimg.com/labis/7f1d85ddbf475fd67afce61368dfb04d~tplv-be4g95zd3a-image.jpeg" alt="风景摄影" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                            <div class="absolute inset-0 bg-black bg-opacity-30 group-hover:bg-opacity-40 transition-colors duration-300"></div>
                            <div class="absolute inset-0 flex items-center justify-center">
                                <h3 class="text-white font-medium text-lg text-shadow">风景</h3>
                            </div>
                        </div>
                    </a>
                    <a href="#" class="category-item group">
                        <div class="relative rounded-xl overflow-hidden h-40">
                            <img src="https://p3-doubao-search-sign.byteimg.com/labis/479287ac6bee78eaed2e3bc77b429759~tplv-be4g95zd3a-image.jpeg" alt="人像摄影" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                            <div class="absolute inset-0 bg-black bg-opacity-30 group-hover:bg-opacity-40 transition-colors duration-300"></div>
                            <div class="absolute inset-0 flex items-center justify-center">
                                <h3 class="text-white font-medium text-lg text-shadow">人像</h3>
                            </div>
                        </div>
                    </a>
                    <a href="#" class="category-item group">
                        <div class="relative rounded-xl overflow-hidden h-40">
                            <img src="https://p3-doubao-search-sign.byteimg.com/labis/7ff49ae9b6c41ed1e201f1060c771c22~tplv-be4g95zd3a-image.jpeg" alt="黑白摄影" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                            <div class="absolute inset-0 bg-black bg-opacity-30 group-hover:bg-opacity-40 transition-colors duration-300"></div>
                            <div class="absolute inset-0 flex items-center justify-center">
                                <h3 class="text-white font-medium text-lg text-shadow">黑白</h3>
                            </div>
                        </div>
                    </a>
                </div>
            </div>
        </section>

        <!-- 页脚 -->
        <footer class="bg-gray-800 dark:bg-gray-900 text-gray-300 py-12">
            <div class="container mx-auto px-4">
                <div class="text-center">
                    <h3 class="text-xl font-bold text-white mb-4">昆仑F5</h3>
                    <p class="mb-4">专业的摄影作品分享平台，邀请制高质量摄影社区。</p>
                    <p>&copy; 2024 昆仑F5摄影社区. All rights reserved. | <a href="https://kunlunF5.com" class="hover:text-white transition-colors">kunlunF5.com</a></p>
                </div>
            </div>
        </footer>
    </main>

    <!-- 所有模态框+JS逻辑（修复本地存储BUG+事件冲突） -->
    <div id="searchModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-start justify-center pt-20 hidden">
        <div class="bg-white dark:bg-gray-800 rounded-lg shadow-xl p-6 max-w-2xl w-full animate-scale-in">
            <div class="flex items-center border-b border-gray-200 dark:border-gray-700 pb-4">
                <i class="fa fa-search text-gray-400 mr-4"></i>
                <input type="text" placeholder="搜索作品、摄影师或标签..." class="flex-1 bg-transparent border-none focus:outline-none text-gray-900 dark:text-white text-lg">
                <button id="searchModalCloseBtn" class="text-gray-400 hover:text-gray-600 dark:hover:text-gray-300">
                    <i class="fa fa-times"></i>
                </button>
            </div>
        </div>
    </div>
    <div id="videoModal" class="fixed inset-0 bg-black bg-opacity-90 z-50 flex items-center justify-center hidden">
        <div class="max-w-4xl w-full px-4">
            <div class="relative">
                <button id="videoModalCloseBtn" class="absolute -top-12 right-0 text-white hover:text-gray-300">
                    <i class="fa fa-times text-2xl"></i>
                </button>
                <div class="bg-black rounded-lg overflow-hidden">
                    <video id="videoPlayer" class="w-full h-auto" controls></video>
                </div>
                <h3 id="videoTitle" class="text-white text-xl font-medium mt-4"></h3>
            </div>
        </div>
    </div>
    <div id="adminLoginModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-center justify-center hidden">
        <div class="bg-white dark:bg-gray-800 rounded-lg shadow-xl p-8 max-w-md w-full animate-scale-in">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white">管理员登录</h3>
                <button id="closeAdminLoginModal" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                    <i class="fa fa-times"></i>
                </button>
            </div>
            <div>
                <div class="mb-4">
                    <label for="adminUsername" class="block text-sm font-medium text-gray-700 dark:text-gray-300">管理员账号</label>
                    <input type="text" id="adminUsername" class="mt-1 block w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 dark:bg-gray-700 dark:text-white">
                </div>
                <div class="mb-6">
                    <label for="adminPassword" class="block text-sm font-medium text-gray-700 dark:text-gray-300">管理员密码</label>
                    <input type="password" id="adminPassword" class="mt-1 block w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 dark:bg-gray-700 dark:text-white">
                </div>
                <button id="submitAdminLogin" class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-red-600 hover:bg-red-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500">
                    管理员登录
                </button>
            </div>
        </div>
    </div>
    <div id="authModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-center justify-center hidden">
        <div class="bg-white dark:bg-gray-800 rounded-lg shadow-xl p-8 max-w-md w-full animate-scale-in">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white" id="authModalTitle">登录</h3>
                <button id="closeAuthModal" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                    <i class="fa fa-times"></i>
                </button>
            </div>
            <div id="loginForm">
                <div class="mb-4">
                    <label for="loginUsername" class="block text-sm font-medium text-gray-700 dark:text-gray-300">用户名</label>
                    <input type="text" id="loginUsername" class="mt-1 block w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 dark:bg-gray-700 dark:text-white">
                </div>
                <div class="mb-6">
                    <label for="loginPassword" class="block text-sm font-medium text-gray-700 dark:text-gray-300">密码</label>
                    <input type="password" id="loginPassword" class="mt-1 block w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 dark:bg-gray-700 dark:text-white">
                </div>
                <button id="submitLogin" class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                    登录
                </button>
            </div>
            <div id="registerForm" class="hidden">
                <div class="mb-4">
                    <label for="registerUsername" class="block text-sm font-medium text-gray-700 dark:text-gray-300">用户名</label>
                    <input type="text" id="registerUsername" class="mt-1 block w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 dark:bg-gray-700 dark:text-white">
                </div>
                <div class="mb-4">
                    <label for="registerInviteCode" class="block text-sm font-medium text-gray-700 dark:text-gray-300">邀请码</label>
                    <input type="text" id="registerInviteCode" class="mt-1 block w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 dark:bg-gray-700 dark:text-white">
                </div>
                <div class="mb-6">
                    <label for="registerPassword" class="block text-sm font-medium text-gray-700 dark:text-gray-300">密码</label>
                    <input type="password" id="registerPassword" class="mt-1 block w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 dark:bg-gray-700 dark:text-white">
                </div>
                <button id="submitRegister" class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                    注册
                </button>
            </div>
            <div class="mt-6 text-center">
                <span id="toggleAuthText" class="text-sm text-gray-600 dark:text-gray-400">
                    还没有账号？ <a href="#" id="toggleAuthForm" class="font-medium text-indigo-600 hover:text-indigo-500 dark:text-indigo-400 dark:hover:text-indigo-300">立即注册</a>
                </span>
            </div>
        </div>
    </div>
    <div id="uploadModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-center justify-center hidden">
        <div class="bg-white dark:bg-gray-800 rounded-lg shadow-xl p-8 max-w-2xl w-full animate-scale-in">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white">上传作品</h3>
                <button id="closeUploadModal" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                    <i class="fa fa-times"></i>
                </button>
            </div>
            <div>
                <div class="mb-4">
                    <label for="uploadTitle" class="block text-sm font-medium text-gray-700 dark:text-gray-300">作品标题</label>
                    <input type="text" id="uploadTitle" class="mt-1 block w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 dark:bg-gray-700 dark:text-white">
                </div>
                <div class="mb-6">
                    <label for="uploadFile" class="block text-sm font-medium text-gray-700 dark:text-gray-300">选择文件</label>
                    <input type="file" id="uploadFile" accept="image/*,video/*" class="mt-1 block w-full text-sm text-gray-500 file:mr-4 file:py-2 file:px-4 file:rounded-md file:border-0 file:text-sm file:font-semibold file:bg-indigo-600 file:text-white hover:file:bg-indigo-700">
                </div>
                <button id="submitUpload" class="w-full flex justify-center py-2 px-4 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500">
                    上传作品
                </button>
            </div>
        </div>
    </div>
    <div id="adminPanelModal" class="fixed inset-0 bg-black bg-opacity-50 z-50 flex items-center justify-center hidden">
        <div class="bg-white dark:bg-gray-800 rounded-lg shadow-xl p-8 max-w-4xl w-full animate-scale-in">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-xl font-bold text-gray-900 dark:text-white">管理员面板</h3>
                <button id="closeAdminPanelModal" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                    <i class="fa fa-times"></i>
                </button>
            </div>
            <div>
                <div class="mb-6">
                    <h4 class="text-lg font-semibold text-gray-900 dark:text-white mb-4">生成邀请码</h4>
                    <div class="flex items-end space-x-4">
                        <div class="flex-1">
                            <label for="inviteCodeCount" class="block text-sm font-medium text-gray-700 dark:text-gray-300">生成数量</label>
                            <input type="number" id="inviteCodeCount" value="1" min="1" max="10" class="mt-1 block w-full px-3 py-2 border border-gray-300 dark:border-gray-600 rounded-md shadow-sm focus:outline-none focus:ring-indigo-500 focus:border-indigo-500 dark:bg-gray-700 dark:text-white">
                        </div>
                        <button id="generateInviteCodes" class="px-4 py-2 border border-transparent rounded-md shadow-sm text-sm font-medium text-white bg-red-600 hover:bg-red-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-red-500">
                            生成邀请码
                        </button>
                    </div>
                </div>
                <div id="inviteCodesList" class="mb-6 hidden">
                    <h4 class="text-lg font-semibold text-gray-900 dark:text-white mb-4">邀请码列表</h4>
                    <div class="bg-gray-50 dark:bg-gray-700 p-4 rounded-md max-h-60 overflow-y-auto">
                        <ul id="inviteCodesListItems" class="list-disc list-inside space-y-2 text-gray-700 dark:text-gray-300">
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            let currentUser = null;
            let isAdmin = false;
            let inviteCodes = ['KUNLUN2024', 'F5PHOTO', 'PHOTOMASTER'];
            const themeToggleBtn = document.getElementById('themeToggleBtn');
            const htmlElement = document.documentElement;
            
            // 修复：本地存储空值判断，兼容首次访问
            const savedTheme = localStorage.getItem('theme');
            if (savedTheme === 'dark' || (!savedTheme && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
                htmlElement.classList.add('dark');
            } else {
                htmlElement.classList.remove('dark');
            }
            
            themeToggleBtn.addEventListener('click', function() {
                htmlElement.classList.toggle('dark');
                localStorage.setItem('theme', htmlElement.classList.contains('dark') ? 'dark' : 'light');
            });

            // 所有菜单/模态框/登录/管理员功能逻辑（完整保留+修复事件冲突）
            const userMenuBtn = document.getElementById('userMenuBtn');
            const userMenu = document.getElementById('userMenu');
            userMenuBtn.addEventListener('click', function(e) {
                e.stopPropagation();
                userMenu.classList.toggle('hidden');
            });
            document.addEventListener('click', function(e) {
                if (!userMenuBtn.contains(e.target) && !userMenu.contains(e.target)) userMenu.classList.add('hidden');
            });

            const filterBtns = document.querySelectorAll('.filter-btn');
            const workItems = document.querySelectorAll('.work-item');
            filterBtns.forEach(btn => {
                btn.addEventListener('click', function() {
                    filterBtns.forEach(item => item.classList.remove('active', 'bg-gray-100', 'dark:bg-gray-700'));
                    this.classList.add('active', 'bg-gray-100', 'dark:bg-gray-700');
                    const filter = this.getAttribute('data-filter');
                    workItems.forEach(item => item.style.display = filter === 'all' || item.classList.contains(filter) ? 'block' : 'none');
                });
            });

            document.getElementById('loginBtn').addEventListener('click', (e)=>{e.preventDefault();document.getElementById('authModal').classList.remove('hidden')});
            document.getElementById('registerBtn').addEventListener('click', (e)=>{e.preventDefault();document.getElementById('authModalTitle').textContent='注册';document.getElementById('loginForm').classList.add('hidden');document.getElementById('registerForm').classList.remove('hidden');document.getElementById('authModal').classList.remove('hidden')});
            document.getElementById('adminLoginBtn').addEventListener('click', (e)=>{e.preventDefault();document.getElementById('adminLoginModal').classList.remove('hidden')});
            document.getElementById('submitAdminLogin').addEventListener('click', ()=>{
                if(document.getElementById('adminUsername').value === 'admin' && document.getElementById('adminPassword').value === 'admin123'){
                    isAdmin=true;document.getElementById('adminLoginModal').classList.add('hidden');document.getElementById('adminPanelModal').classList.remove('hidden');
                }else alert('账号密码错误！管理员账号：admin，密码：admin123');
            });
            document.getElementById('submitLogin').addEventListener('click', ()=>{
                if(document.getElementById('loginUsername').value && document.getElementById('loginPassword').value){
                    currentUser={username:document.getElementById('loginUsername').value};
                    document.getElementById('authModal').classList.add('hidden');
                    document.getElementById('userMenuBtn').querySelector('span').textContent=currentUser.username;
                    document.getElementById('loginBtn').classList.add('hidden');
                    document.getElementById('registerBtn').classList.add('hidden');
                    document.getElementById('uploadBtn').classList.remove('hidden');
                    document.getElementById('logoutBtn').classList.remove('hidden');
                    alert('登录成功！');
                }else alert('请填写账号密码');
            });
            document.getElementById('submitRegister').addEventListener('click', ()=>{
                if(document.getElementById('registerInviteCode').value && inviteCodes.includes(document.getElementById('registerInviteCode').value)){
                    currentUser={username:document.getElementById('registerUsername').value};
                    document.getElementById('authModal').classList.add('hidden');
                    alert('注册成功！');
                }else alert('邀请码无效！');
            });
            document.getElementById('generateInviteCodes').addEventListener('click', ()=>{
                const count = parseInt(document.getElementById('inviteCodeCount').value);
                const newCodes = [];
                for(let i=0;i<count;i++){const code='KUNLUN'+Math.random().toString(36).substr(2,9).toUpperCase();newCodes.push(code);inviteCodes.push(code);}
                document.getElementById('inviteCodesListItems').innerHTML=newCodes.map(c=>`<li>${c}</li>`).join('');
                document.getElementById('inviteCodesList').classList.remove('hidden');
            });
            document.getElementById('uploadBtn').addEventListener('click', (e)=>{e.preventDefault();document.getElementById('uploadModal').classList.remove('hidden')});
            document.getElementById('submitUpload').addEventListener('click', ()=>{
                if(document.getElementById('uploadTitle').value && document.getElementById('uploadFile').files.length){
                    document.getElementById('uploadModal').classList.add('hidden');alert('作品上传成功！');
                }else alert('请填写标题并选择文件');
            });
            document.getElementById('logoutBtn').addEventListener('click', (e)=>{
                e.preventDefault();currentUser=null;
                document.getElementById('userMenuBtn').querySelector('span').textContent='登录';
                document.getElementById('loginBtn').classList.remove('hidden');
                document.getElementById('registerBtn').classList.remove('hidden');
                document.getElementById('uploadBtn').classList.add('hidden');
                document.getElementById('logoutBtn').classList.add('hidden');
                alert('已退出登录');
            });
            // 关闭所有模态框的按钮
            document.querySelectorAll('[id*=close]').forEach(btn=>btn.addEventListener('click', ()=>{btn.closest('[id*=Modal]').classList.add('hidden')}));
        });
    </script>
</body>
</html>
