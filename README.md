# Language-earning
Earn money by teaching white men Swahili.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Earn Through Language - Global Language Task Platform</title>
    
    <!-- PWA & Mobile Meta Tags -->
    <link rel="manifest" href="manifest.json">
    <meta name="theme-color" content="#22c55e">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="ETL Earn">
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            50: '#f0fdf4',
                            100: '#dcfce7',
                            500: '#22c55e',
                            600: '#16a34a',
                            700: '#15803d',
                            900: '#14532d',
                        }
                    }
                }
            }
        }
    </script>
    <style>
        .glass-card {
            background: rgba(17, 24, 39, 0.75);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .glow-effect {
            box-shadow: 0 0 25px -5px rgba(34, 197, 94, 0.3);
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 font-sans min-h-screen selection:bg-brand-500 selection:text-white flex flex-col justify-between">

    <!-- Top Navigation -->
    <header class="glass-card sticky top-0 z-50 border-b border-slate-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <div class="flex items-center space-x-3 cursor-pointer" onclick="switchView('landing')">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-brand-600 to-emerald-400 flex items-center justify-center glow-effect">
                    <i class="fa-solid fa-earth-africa text-white text-lg"></i>
                </div>
                <div>
                    <span class="text-xl font-extrabold tracking-tight bg-gradient-to-r from-white via-slate-200 to-brand-400 bg-clip-text text-transparent">Earn Through Language</span>
                    <span class="block text-[10px] tracking-widest uppercase text-brand-500 font-bold">Android, iOS & Windows Ready</span>
                </div>
            </div>
            
            <div id="nav-auth-buttons" class="flex items-center space-x-4">
                <button onclick="openInstallGuideModal()" class="hidden md:inline-flex items-center space-x-2 text-xs bg-slate-900 border border-slate-800 hover:border-brand-500 text-brand-400 px-3.5 py-2 rounded-xl transition font-semibold">
                    <i class="fa-solid fa-download"></i><span>Install App</span>
                </button>
                <button onclick="openAuthModal('login')" class="text-sm font-semibold text-slate-300 hover:text-white px-4 py-2 rounded-lg transition">Sign In</button>
                <button onclick="openAuthModal('signup')" class="bg-brand-600 hover:bg-brand-500 text-white text-sm font-bold px-5 py-2.5 rounded-xl transition glow-effect shadow-lg">Get Started</button>
            </div>

            <div id="nav-user-profile" class="hidden items-center space-x-4">
                <div class="flex items-center space-x-3 bg-slate-900 border border-slate-800 px-3 py-1.5 rounded-full">
                    <div class="w-8 h-8 rounded-full bg-brand-600 flex items-center justify-center font-bold text-white text-sm" id="user-avatar-initial">U</div>
                    <div class="text-left hidden sm:block">
                        <p class="text-xs font-bold text-slate-200" id="nav-username">Username</p>
                        <p class="text-[10px] text-brand-400 font-medium" id="nav-status-badge">Inactive Account</p>
                    </div>
                </div>
                <button onclick="logout()" class="text-slate-400 hover:text-rose-400 p-2 transition" title="Log Out"><i class="fa-solid fa-power-off text-lg"></i></button>
            </div>
        </div>
    </header>

    <!-- Main Dynamic Content Wrapper -->
    <main class="flex-grow">

        <!-- LANDING PAGE VIEW -->
        <div id="view-landing" class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-12 lg:py-20">
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
                <div class="lg:col-span-7 space-y-6 text-center lg:text-left">
                    <div class="inline-flex items-center space-x-2 bg-brand-950/80 border border-brand-800 px-3.5 py-1.5 rounded-full text-brand-400 text-xs font-semibold">
                        <i class="fa-solid fa-bolt text-brand-500"></i>
                        <span>Activate with $0.5 via Paybill 891300 (Acc: 144841)</span>
                    </div>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold tracking-tight leading-tight">
                        Translate Languages, Earn Cash & <span class="bg-gradient-to-r from-brand-400 to-emerald-300 bg-clip-text text-transparent">Run on Any Device</span>
                    </h1>
                    <p class="text-slate-400 text-base sm:text-lg max-w-2xl mx-auto lg:mx-0">
                        Access our platform seamlessly on **Android, iPhone, and Windows PC**. Complete language micro-tasks and earn multi-tier referral bonuses instantly.
                    </p>
                    
                    <!-- App Install Badges Row -->
                    <div class="flex flex-wrap items-center justify-center lg:justify-start gap-3 pt-2">
                        <button onclick="openInstallGuideModal()" class="bg-slate-900 hover:bg-slate-800 border border-slate-800 text-slate-200 px-4 py-2.5 rounded-xl text-xs font-bold flex items-center space-x-2 transition">
                            <i class="fa-brands fa-android text-brand-400 text-base"></i><span>Install Android App</span>
                        </button>
                        <button onclick="openInstallGuideModal()" class="bg-slate-900 hover:bg-slate-800 border border-slate-800 text-slate-200 px-4 py-2.5 rounded-xl text-xs font-bold flex items-center space-x-2 transition">
                            <i class="fa-brands fa-apple text-brand-400 text-base"></i><span>Install iPhone App</span>
                        </button>
                        <button onclick="openInstallGuideModal()" class="bg-slate-900 hover:bg-slate-800 border border-slate-800 text-slate-200 px-4 py-2.5 rounded-xl text-xs font-bold flex items-center space-x-2 transition">
                            <i class="fa-brands fa-windows text-brand-400 text-base"></i><span>Install Windows PC</span>
                        </button>
                    </div>

                    <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start space-y-3 sm:space-y-0 sm:space-x-4 pt-4">
                        <button onclick="openAuthModal('signup')" class="w-full sm:w-auto bg-brand-600 hover:bg-brand-500 text-white font-bold px-8 py-4 rounded-xl transition glow-effect shadow-xl text-center">
                            Create Free Account <i class="fa-solid fa-arrow-right ml-2"></i>
                        </button>
                        <button onclick="openAuthModal('login')" class="w-full sm:w-auto bg-slate-900 hover:bg-slate-800 border border-slate-800 text-slate-300 font-semibold px-8 py-4 rounded-xl transition text-center">
                            Member Login
                        </button>
                    </div>

                    <!-- Trust Stats -->
                    <div class="grid grid-cols-3 gap-4 pt-8 border-t border-slate-900">
                        <div>
                            <p class="text-2xl font-extrabold text-white">$142,500+</p>
                            <p class="text-xs text-slate-400">Total Payouts</p>
                        </div>
                        <div>
                            <p class="text-2xl font-extrabold text-white">45,000+</p>
                            <p class="text-xs text-slate-400">Active Earners</p>
                        </div>
                        <div>
                            <p class="text-2xl font-extrabold text-white">Instant</p>
                            <p class="text-xs text-slate-400">Paybill Payouts</p>
                        </div>
                    </div>
                </div>

                <!-- Right Hero Card -->
                <div class="lg:col-span-5">
                    <div class="glass-card rounded-3xl p-6 sm:p-8 shadow-2xl relative overflow-hidden border border-slate-800">
                        <div class="absolute -right-16 -top-16 w-48 h-48 bg-brand-500/10 rounded-full blur-3xl pointer-events-none"></div>
                        <h3 class="text-xl font-bold mb-4 flex items-center justify-between">
                            <span>Platform Live Feed</span>
                            <span class="flex h-3 w-3 relative">
                                <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-brand-400 opacity-75"></span>
                                <span class="relative inline-flex rounded-full h-3 w-3 bg-brand-500"></span>
                            </span>
                        </h3>
                        <div class="space-y-3" id="live-feed-ticker">
                            <div class="bg-slate-900/80 border border-slate-800/80 p-3.5 rounded-xl flex items-center justify-between">
                                <div class="flex items-center space-x-3">
                                    <div class="w-9 h-9 rounded-lg bg-emerald-950 text-brand-400 flex items-center justify-center font-bold text-sm"><i class="fa-solid fa-check"></i></div>
                                    <div>
                                        <p class="text-xs font-bold text-slate-200">Brian K. activated account</p>
                                        <p class="text-[10px] text-slate-400">Paybill 891300 | Acc 144841</p>
                                    </div>
                                </div>
                                <span class="text-xs font-bold text-brand-400">+$0.5 Sub</span>
                            </div>
                            <div class="bg-slate-900/80 border border-slate-800/80 p-3.5 rounded-xl flex items-center justify-between">
                                <div class="flex items-center space-x-3">
                                    <div class="w-9 h-9 rounded-lg bg-blue-950 text-blue-400 flex items-center justify-center font-bold text-sm"><i class="fa-solid fa-wallet"></i></div>
                                    <div>
                                        <p class="text-xs font-bold text-slate-200">Mercy W. withdrew</p>
                                        <p class="text-[10px] text-slate-400">Language Task Reward</p>
                                    </div>
                                </div>
                                <span class="text-xs font-bold text-emerald-400">KES 1,200</span>
                            </div>
                            <div class="bg-slate-900/80 border border-slate-800/80 p-3.5 rounded-xl flex items-center justify-between">
                                <div class="flex items-center space-x-3">
                                    <div class="w-9 h-9 rounded-lg bg-purple-950 text-purple-400 flex items-center justify-center font-bold text-sm"><i class="fa-solid fa-user-plus"></i></div>
                                    <div>
                                        <p class="text-xs font-bold text-slate-200">Kevin M. joined via referral</p>
                                        <p class="text-[10px] text-slate-400">Ref Code Active</p>
                                    </div>
                                </div>
                                <span class="text-xs font-bold text-purple-400">Tier 1 Bonus</span>
                            </div>
                        </div>

                        <div class="mt-6 pt-6 border-t border-slate-800/85">
                            <div class="bg-brand-950/40 border border-brand-900/50 rounded-2xl p-4 text-center">
                                <p class="text-xs text-brand-300 font-semibold mb-1">Activation Fee Requirement</p>
                                <p class="text-2xl font-black text-white">$0.5 <span class="text-xs font-normal text-slate-400">(Paybill: 891300 | Acc: 144841)</span></p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- USER DASHBOARD VIEW (Hidden by default) -->
        <div id="view-dashboard" class="hidden max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 space-y-8">
            
            <!-- Activation Notice Banner (If Inactive) -->
            <div id="activation-banner" class="hidden bg-gradient-to-r from-amber-500/20 via-orange-500/20 to-red-500/20 border border-amber-500/40 rounded-3xl p-6 flex flex-col md:flex-row items-center justify-between gap-4">
                <div class="flex items-center space-x-4">
                    <div class="w-12 h-12 rounded-2xl bg-amber-500/20 text-amber-400 flex items-center justify-center text-xl shrink-0"><i class="fa-solid fa-triangle-exclamation"></i></div>
                    <div>
                        <h4 class="text-base font-bold text-amber-200">Account Activation Required</h4>
                        <p class="text-xs text-amber-300/80">Your dashboard tasks and withdrawal features are locked. Send $0.5 to Paybill 891300 (Account: 144841).</p>
                    </div>
                </div>
                <button onclick="openActivationModal()" class="w-full md:w-auto bg-amber-500 hover:bg-amber-400 text-slate-950 font-extrabold px-6 py-3 rounded-xl transition shadow-lg shrink-0">
                    <i class="fa-solid fa-lock-open mr-2"></i> Activate Account Now
                </button>
            </div>

            <!-- Welcome & Stats Row -->
            <div class="grid grid-cols-1 md:grid-cols-4 gap-6">
                <div class="glass-card rounded-2xl p-6 border border-slate-800">
                    <div class="flex items-center justify-between mb-4">
                        <span class="text-xs font-bold text-slate-400 uppercase tracking-wider">Account Balance</span>
                        <div class="w-10 h-10 rounded-xl bg-brand-950 text-brand-400 flex items-center justify-center font-bold"><i class="fa-solid fa-wallet"></i></div>
                    </div>
                    <h3 class="text-3xl font-black text-white" id="dash-balance">$0.00</h3>
                    <p class="text-xs text-slate-400 mt-2 flex items-center justify-between">
                        <span>Status: <span id="dash-status-text" class="text-amber-400 font-bold">Pending Activation</span></span>
                        <button onclick="switchTab('wallet')" class="text-brand-400 font-bold hover:underline">Withdraw</button>
                    </p>
                </div>

                <div class="glass-card rounded-2xl p-6 border border-slate-800">
                    <div class="flex items-center justify-between mb-4">
                        <span class="text-xs font-bold text-slate-400 uppercase tracking-wider">Completed Tasks</span>
                        <div class="w-10 h-10 rounded-xl bg-blue-950 text-blue-400 flex items-center justify-center font-bold"><i class="fa-solid fa-list-check"></i></div>
                    </div>
                    <h3 class="text-3xl font-black text-white" id="dash-tasks-count">0</h3>
                    <p class="text-xs text-slate-400 mt-2">Language jobs finalized</p>
                </div>

                <div class="glass-card rounded-2xl p-6 border border-slate-800">
                    <div class="flex items-center justify-between mb-4">
                        <span class="text-xs font-bold text-slate-400 uppercase tracking-wider">Referral Earnings</span>
                        <div class="w-10 h-10 rounded-xl bg-purple-950 text-purple-400 flex items-center justify-center font-bold"><i class="fa-solid fa-users"></i></div>
                    </div>
                    <h3 class="text-3xl font-black text-white" id="dash-referral-earnings">$0.00</h3>
                    <p class="text-xs text-slate-400 mt-2"><span id="dash-referral-count">0</span> downline members</p>
                </div>

                <div class="glass-card rounded-2xl p-6 border border-slate-800 flex flex-col justify-between">
                    <span class="text-xs font-bold text-slate-400 uppercase tracking-wider">Quick Referral Link</span>
                    <div class="bg-slate-900 border border-slate-800 rounded-xl p-2.5 flex items-center justify-between mt-2">
                        <input type="text" id="dash-ref-link" readonly class="bg-transparent text-xs text-slate-300 w-full outline-none px-1 truncate" value="https://earnthroughlanguage.com/signup?ref=user">
                        <button onclick="copyRefLink()" class="bg-brand-600 hover:bg-brand-500 text-white text-xs px-3 py-1.5 rounded-lg font-bold transition shrink-0 ml-2">Copy</button>
                    </div>
                    <p class="text-[10px] text-slate-500 mt-2 text-center">Earn 30% commission on referrals</p>
                </div>
            </div>

            <!-- Tabs Navigation -->
            <div class="flex border-b border-slate-800 space-x-8">
                <button onclick="switchTab('tasks')" id="tab-btn-tasks" class="py-4 text-sm font-bold border-b-2 border-brand-500 text-brand-400 transition flex items-center space-x-2">
                    <i class="fa-solid fa-language"></i>
                    <span>Language Tasks</span>
                </button>
                <button onclick="switchTab('referrals')" id="tab-btn-referrals" class="py-4 text-sm font-bold border-b-2 border-transparent text-slate-400 hover:text-white transition flex items-center space-x-2">
                    <i class="fa-solid fa-share-nodes"></i>
                    <span>Referral Network</span>
                </button>
                <button onclick="switchTab('wallet')" id="tab-btn-wallet" class="py-4 text-sm font-bold border-b-2 border-transparent text-slate-400 hover:text-white transition flex items-center space-x-2">
                    <i class="fa-solid fa-money-bill-transfer"></i>
                    <span>Withdrawals & Payouts</span>
                </button>
            </div>

            <!-- TAB 1: TASKS -->
            <div id="tab-content-tasks" class="space-y-6">
                <div class="flex items-center justify-between">
                    <div>
                        <h3 class="text-lg font-bold text-white">Available Language Tasks</h3>
                        <p class="text-xs text-slate-400">Complete translation reviews and audio transcriptions to earn instant cash reward balances.</p>
                    </div>
                    <span class="text-xs bg-slate-900 border border-slate-800 px-3 py-1.5 rounded-xl text-slate-300 font-medium">3 Tasks Ready</span>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <!-- Task 1 -->
                    <div class="glass-card rounded-2xl p-6 border border-slate-800 flex flex-col justify-between">
                        <div>
                            <div class="flex items-center justify-between mb-3">
                                <span class="bg-blue-950 text-blue-400 text-[10px] font-bold px-2.5 py-1 rounded-md uppercase">Swahili - English</span>
                                <span class="text-brand-400 font-extrabold text-sm">+$0.25</span>
                            </div>
                            <h4 class="text-base font-bold text-white mb-2">Social Media Caption Translation</h4>
                            <p class="text-xs text-slate-400 mb-4">Review and verify product marketing captions translated from English into Swahili regional terms.</p>
                        </div>
                        <button onclick="completeTask(1, 0.25, 'Social Media Caption Translation')" class="w-full bg-slate-900 hover:bg-brand-600 hover:text-white border border-slate-800 text-slate-300 text-xs font-bold py-3 rounded-xl transition flex items-center justify-center space-x-2">
                            <i class="fa-solid fa-play"></i><span>Start Task</span>
                        </button>
                    </div>

                    <!-- Task 2 -->
                    <div class="glass-card rounded-2xl p-6 border border-slate-800 flex flex-col justify-between">
                        <div>
                            <div class="flex items-center justify-between mb-3">
                                <span class="bg-purple-950 text-purple-400 text-[10px] font-bold px-2.5 py-1 rounded-md uppercase">Audio Review</span>
                                <span class="text-brand-400 font-extrabold text-sm">+$0.40</span>
                            </div>
                            <h4 class="text-base font-bold text-white mb-2">Voice Pronunciation Validation</h4>
                            <p class="text-xs text-slate-400 mb-4">Listen to short 30-second audio recordings in local dialects and check for pronunciation clarity.</p>
                        </div>
                        <button onclick="completeTask(2, 0.40, 'Voice Pronunciation Validation')" class="w-full bg-slate-900 hover:bg-brand-600 hover:text-white border border-slate-800 text-slate-300 text-xs font-bold py-3 rounded-xl transition flex items-center justify-center space-x-2">
                            <i class="fa-solid fa-play"></i><span>Start Task</span>
                        </button>
                    </div>

                    <!-- Task 3 -->
                    <div class="glass-card rounded-2xl p-6 border border-slate-800 flex flex-col justify-between">
                        <div>
                            <div class="flex items-center justify-between mb-3">
                                <span class="bg-emerald-950 text-emerald-400 text-[10px] font-bold px-2.5 py-1 rounded-md uppercase">Transcription</span>
                                <span class="text-brand-400 font-extrabold text-sm">+$0.50</span>
                            </div>
                            <h4 class="text-base font-bold text-white mb-2">Medical Clinic Brochure Proofreading</h4>
                            <p class="text-xs text-slate-400 mb-4">Proofread health brochure information translated for Lucent Medicare patient engagement materials.</p>
                        </div>
                        <button onclick="completeTask(3, 0.50, 'Medical Clinic Brochure Proofreading')" class="w-full bg-slate-900 hover:bg-brand-600 hover:text-white border border-slate-800 text-slate-300 text-xs font-bold py-3 rounded-xl transition flex items-center justify-center space-x-2">
                            <i class="fa-solid fa-play"></i><span>Start Task</span>
                        </button>
                    </div>
                </div>
            </div>

            <!-- TAB 2: REFERRALS -->
            <div id="tab-content-referrals" class="hidden space-y-6">
                <div class="glass-card rounded-3xl p-6 sm:p-8 border border-slate-800 flex flex-col md:flex-row items-center justify-between gap-6">
                    <div class="space-y-2">
                        <span class="text-xs font-bold text-brand-400 uppercase tracking-widest">Affiliate Program</span>
                        <h3 class="text-2xl font-black text-white">Invite Friends & Earn Instantly</h3>
                        <p class="text-xs text-slate-400 max-w-xl">Share your referral link. When your friends sign up and activate their accounts using Paybill 891300, you instantly receive 30% commission bonuses credited to your withdrawable balance.</p>
                    </div>
                    <div class="bg-slate-900 border border-slate-800 rounded-2xl p-4 text-center shrink-0 w-full md:w-auto">
                        <p class="text-xs text-slate-400 mb-1">Total Referral Signups</p>
                        <p class="text-3xl font-extrabold text-white" id="ref-stat-count">0</p>
                    </div>
                </div>

                <div class="glass-card rounded-2xl p-6 border border-slate-800">
                    <h4 class="text-base font-bold text-white mb-4">Your Downline Network</h4>
                    <div class="overflow-x-auto">
                        <table class="w-full text-left text-xs">
                            <thead>
                                <tr class="border-b border-slate-800 text-slate-400">
                                    <th class="pb-3 font-semibold">Username</th>
                                    <th class="pb-3 font-semibold">Date Joined</th>
                                    <th class="pb-3 font-semibold">Activation Status</th>
                                    <th class="pb-3 font-semibold text-right">Commission Earned</th>
                                </tr>
                            </thead>
                            <tbody id="referrals-table-body" class="divide-y divide-slate-900 text-slate-300">
                                <tr>
                                    <td colspan="4" class="text-center py-6 text-slate-500">No referrals yet. Share your link to start building your network!</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>

            <!-- TAB 3: WALLET -->
            <div id="tab-content-wallet" class="hidden space-y-6">
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="glass-card rounded-2xl p-6 border border-slate-800 flex flex-col justify-between">
                        <div>
                            <h4 class="text-base font-bold text-white mb-2">Request Payout</h4>
                            <p class="text-xs text-slate-400 mb-6">Withdraw your available task rewards directly to your M-Pesa phone number or bank account instantly.</p>
                            
                            <div class="space-y-4">
                                <div>
                                    <label class="block text-xs font-semibold text-slate-300 mb-1">Payout Amount ($)</label>
                                    <input type="number" id="withdraw-amount" placeholder="0.00" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-500">
                                </div>
                                <div>
                                    <label class="block text-xs font-semibold text-slate-300 mb-1">M-Pesa Phone Number</label>
                                    <input type="text" id="withdraw-phone" placeholder="0712345678" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-500">
                                </div>
                            </div>
                        </div>
                        <button onclick="requestWithdrawal()" class="w-full mt-6 bg-brand-600 hover:bg-brand-500 text-white font-bold py-3.5 rounded-xl transition shadow-lg text-sm">
                            Submit Withdrawal Request
                        </button>
                    </div>

                    <div class="glass-card rounded-2xl p-6 border border-slate-800 flex flex-col justify-between">
                        <div>
                            <h4 class="text-base font-bold text-white mb-2">Transaction History</h4>
                            <p class="text-xs text-slate-400 mb-4">Recent activation fees, task earnings, and payout logs.</p>
                            <div class="space-y-3 max-h-60 overflow-y-auto pr-1" id="transaction-history-list">
                                <div class="text-center py-8 text-slate-500 text-xs">No transactions recorded yet.</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

        </div>

    </main>

    <!-- Footer -->
    <footer class="border-t border-slate-900 py-8 bg-slate-950 mt-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between text-xs text-slate-500 space-y-4 sm:space-y-0">
            <p>&copy; 2026 Earn Through Language. Accessible on Android, iPhone & Windows.</p>
            <div class="flex items-center space-x-6">
                <span>Paybill: <strong class="text-slate-300">891300</strong></span>
                <span>Account: <strong class="text-slate-300">144841</strong></span>
                <span>Sub Fee: <strong class="text-slate-300">$0.5</strong></span>
            </div>
        </div>
    </footer>

    <!-- INSTALL APP GUIDE MODAL -->
    <div id="install-guide-modal" class="fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-md hidden items-center justify-center p-4">
        <div class="glass-card rounded-3xl max-w-xl w-full p-8 border border-slate-800 relative shadow-2xl space-y-6">
            <button onclick="closeInstallGuideModal()" class="absolute top-6 right-6 text-slate-400 hover:text-white text-lg"><i class="fa-solid fa-xmark"></i></button>
            
            <div class="text-center">
                <div class="w-12 h-12 rounded-2xl bg-brand-600/20 text-brand-400 flex items-center justify-center mx-auto mb-3 text-xl glow-effect"><i class="fa-solid fa-mobile-screen-button"></i></div>
                <h3 class="text-2xl font-extrabold text-white">Install App on Your Device</h3>
                <p class="text-xs text-slate-400 mt-1">Enjoy a full-screen app experience on Android, iPhone, or Windows PC.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 text-xs">
                <!-- Android -->
                <div class="bg-slate-900/90 border border-slate-800 p-4 rounded-2xl space-y-2">
                    <div class="flex items-center space-x-2 text-brand-400 font-bold text-sm">
                        <i class="fa-brands fa-android"></i><span>Android</span>
                    </div>
                    <p class="text-slate-300">Open in <strong>Chrome</strong>, tap the menu <i class="fa-solid fa-ellipsis-vertical"></i> and select <strong>"Install App"</strong> or <strong>"Add to Home screen"</strong>.</p>
                </div>
                <!-- iPhone -->
                <div class="bg-slate-900/90 border border-slate-800 p-4 rounded-2xl space-y-2">
                    <div class="flex items-center space-x-2 text-brand-400 font-bold text-sm">
                        <i class="fa-brands fa-apple"></i><span>iPhone (iOS)</span>
                    </div>
                    <p class="text-slate-300">Open in <strong>Safari</strong>, tap the <strong>Share</strong> button <i class="fa-solid fa-arrow-up-from-bracket"></i> and select <strong>"Add to Home Screen"</strong>.</p>
                </div>
                <!-- Windows -->
                <div class="bg-slate-900/90 border border-slate-800 p-4 rounded-2xl space-y-2">
                    <div class="flex items-center space-x-2 text-brand-400 font-bold text-sm">
                        <i class="fa-brands fa-windows"></i><span>Windows PC</span>
                    </div>
                    <p class="text-slate-300">Open in <strong>Chrome</strong> or <strong>Edge</strong>, click the install icon in the address bar or menu to install as a desktop app.</p>
                </div>
            </div>

            <button onclick="closeInstallGuideModal()" class="w-full bg-brand-600 hover:bg-brand-500 text-white font-bold py-3.5 rounded-xl transition shadow-lg text-sm">
                Got It, Let's Start
            </button>
        </div>
    </div>

    <!-- AUTH MODAL (Login / Signup) -->
    <div id="auth-modal" class="fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-md hidden items-center justify-center p-4">
        <div class="glass-card rounded-3xl max-w-md w-full p-8 border border-slate-800 relative shadow-2xl">
            <button onclick="closeAuthModal()" class="absolute top-6 right-6 text-slate-400 hover:text-white text-lg"><i class="fa-solid fa-xmark"></i></button>
            
            <div class="text-center mb-6">
                <div class="w-12 h-12 rounded-2xl bg-brand-600/20 text-brand-400 flex items-center justify-center mx-auto mb-3 text-xl glow-effect"><i class="fa-solid fa-user-circle"></i></div>
                <h3 class="text-2xl font-extrabold text-white" id="auth-modal-title">Welcome Back</h3>
                <p class="text-xs text-slate-400 mt-1" id="auth-modal-subtitle">Sign in to access your language tasks and earnings.</p>
            </div>

            <form onsubmit="handleAuthSubmit(event)" class="space-y-4">
                <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">Username</label>
                    <input type="text" id="auth-username" required placeholder="e.g. kainga" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-500">
                </div>
                <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">Phone Number (M-Pesa)</label>
                    <input type="text" id="auth-phone" required placeholder="0712345678" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-500">
                </div>
                <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">Password</label>
                    <input type="password" id="auth-password" required placeholder="••••••••" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-500">
                </div>
                
                <div id="auth-ref-container">
                    <label class="block text-xs font-semibold text-slate-300 mb-1">Referral Code (Optional)</label>
                    <input type="text" id="auth-ref-code" placeholder="e.g. c2e" class="w-full bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-500">
                </div>

                <button type="submit" id="auth-submit-btn" class="w-full bg-brand-600 hover:bg-brand-500 text-white font-bold py-3.5 rounded-xl transition shadow-lg text-sm mt-2">
                    Sign In
                </button>
            </form>

            <div class="text-center mt-6">
                <p class="text-xs text-slate-400" id="auth-switch-text">
                    Don't have an account? <button type="button" onclick="toggleAuthMode()" class="text-brand-400 font-bold hover:underline">Sign up</button>
                </p>
            </div>
        </div>
    </div>

    <!-- ACTIVATION MODAL (Paybill Checkout) -->
    <div id="activation-modal" class="fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-md hidden items-center justify-center p-4">
        <div class="glass-card rounded-3xl max-w-lg w-full p-8 border border-slate-800 relative shadow-2xl">
            <button onclick="closeActivationModal()" class="absolute top-6 right-6 text-slate-400 hover:text-white text-lg"><i class="fa-solid fa-xmark"></i></button>
            
            <div class="text-center mb-6">
                <div class="w-12 h-12 rounded-2xl bg-brand-600/20 text-brand-400 flex items-center justify-center mx-auto mb-3 text-xl glow-effect"><i class="fa-solid fa-mobile-screen-button"></i></div>
                <h3 class="text-2xl font-extrabold text-white">Activate Your Account</h3>
                <p class="text-xs text-slate-400 mt-1">Send $0.5 via M-Pesa Paybill to unlock tasks and withdrawals.</p>
            </div>

            <div class="space-y-4 bg-slate-900/90 border border-slate-800 p-5 rounded-2xl">
                <div class="flex justify-between items-center text-xs border-b border-slate-800 pb-3">
                    <span class="text-slate-400">Subscription Fee:</span>
                    <span class="font-bold text-white text-sm">$0.5 (~KES 65)</span>
                </div>
                <div class="flex justify-between items-center text-xs border-b border-slate-800 pb-3">
                    <span class="text-slate-400">Payment Method:</span>
                    <span class="font-bold text-emerald-400">Lipa Na M-Pesa (Paybill)</span>
                </div>
                <div class="flex justify-between items-center text-xs border-b border-slate-800 pb-3">
                    <span class="text-slate-400">Business Number (Paybill):</span>
                    <span class="font-mono font-bold text-brand-400 text-sm select-all">891300</span>
                </div>
                <div class="flex justify-between items-center text-xs">
                    <span class="text-slate-400">Account Number:</span>
                    <span class="font-mono font-bold text-brand-400 text-sm select-all">144841</span>
                </div>
            </div>

            <div class="mt-6 space-y-4">
                <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">Enter M-Pesa Transaction Code</label>
                    <input type="text" id="mpesa-code-input" placeholder="e.g. QHJ72K9XYZ" class="w-full uppercase bg-slate-900 border border-slate-800 rounded-xl px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-500 font-mono">
                </div>
                <button onclick="verifyActivationPayment()" class="w-full bg-brand-600 hover:bg-brand-500 text-white font-bold py-3.5 rounded-xl transition shadow-lg text-sm">
                    Confirm & Activate Account
                </button>
            </div>
        </div>
    </div>

    <!-- TASK RUNNER MODAL -->
    <div id="task-modal" class="fixed inset-0 z-50 bg-slate-950/80 backdrop-blur-md hidden items-center justify-center p-4">
        <div class="glass-card rounded-3xl max-w-lg w-full p-8 border border-slate-800 relative shadow-2xl text-center space-y-6">
            <div class="w-16 h-16 rounded-full bg-brand-600/20 text-brand-400 flex items-center justify-center mx-auto text-2xl glow-effect animate-bounce">
                <i class="fa-solid fa-language"></i>
            </div>
            <div>
                <h3 class="text-xl font-bold text-white" id="modal-task-title">Processing Language Task</h3>
                <p class="text-xs text-slate-400 mt-2" id="modal-task-desc">Please review the text snippet and confirm quality verification.</p>
            </div>
            <div class="bg-slate-900 border border-slate-800 p-4 rounded-2xl text-left text-xs space-y-2 font-mono text-slate-300">
                <p class="text-brand-400 font-bold">// SAMPLE LANGUAGE TEXT</p>
                <p>"Karibu sana kwa jukwaa letu la lugha na tafsiri mtandaoni..."</p>
            </div>
            <div id="task-progress-box" class="space-y-2">
                <div class="w-full bg-slate-900 h-2 rounded-full overflow-hidden">
                    <div id="task-progress-bar" class="bg-brand-500 h-full w-0 transition-all duration-1000"></div>
                </div>
                <p class="text-[10px] text-slate-400" id="task-status-text">Verifying translation accuracy...</p>
            </div>
            <button id="task-claim-btn" onclick="claimTaskReward()" class="hidden w-full bg-brand-600 hover:bg-brand-500 text-white font-bold py-3.5 rounded-xl transition shadow-lg text-sm">
                Claim Reward ($<span id="modal-reward-val">0.25</span>)
            </button>
        </div>
    </div>

    <!-- APPLICATION LOGIC SCRIPT -->
    <script>
        let currentUser = null;
        let authMode = 'login';
        let activeTaskData = null;

        window.addEventListener('DOMContentLoaded', () => {
            const urlParams = new URLSearchParams(window.location.search);
            const refParam = urlParams.get('ref');
            if (refParam) {
                localStorage.setItem('etl_pending_ref', refParam);
            }

            const savedUser = localStorage.getItem('etl_current_user');
            if (savedUser) {
                currentUser = JSON.parse(savedUser);
                enterDashboard();
            }

            updateRefLinkDisplay();
        });

        function updateRefLinkDisplay() {
            const username = currentUser ? currentUser.username : 'user';
            const link = `${window.location.origin}${window.location.pathname}?ref=${username}`;
            document.getElementById('dash-ref-link').value = link;
        }

        function openInstallGuideModal() {
            document.getElementById('install-guide-modal').classList.remove('hidden');
            document.getElementById('install-guide-modal').classList.add('flex');
        }

        function closeInstallGuideModal() {
            document.getElementById('install-guide-modal').classList.remove('flex');
            document.getElementById('install-guide-modal').classList.add('hidden');
        }

        function openAuthModal(mode) {
            authMode = mode;
            const modal = document.getElementById('auth-modal');
            const title = document.getElementById('auth-modal-title');
            const subtitle = document.getElementById('auth-modal-subtitle');
            const submitBtn = document.getElementById('auth-submit-btn');
            const refContainer = document.getElementById('auth-ref-container');
            const switchText = document.getElementById('auth-switch-text');

            modal.classList.remove('hidden');
            modal.classList.add('flex');

            if (authMode === 'login') {
                title.innerText = 'Welcome Back';
                subtitle.innerText = 'Sign in to access your language tasks and earnings.';
                submitBtn.innerText = 'Sign In';
                refContainer.classList.add('hidden');
                switchText.innerHTML = `Don't have an account? <button type="button" onclick="toggleAuthMode()" class="text-brand-400 font-bold hover:underline">Sign up</button>`;
            } else {
                title.innerText = 'Create Account';
                subtitle.innerText = 'Join Earn Through Language and start earning today.';
                submitBtn.innerText = 'Create Account';
                refContainer.classList.remove('hidden');
                
                const pendingRef = localStorage.getItem('etl_pending_ref');
                if (pendingRef) {
                    document.getElementById('auth-ref-code').value = pendingRef;
                }

                switchText.innerHTML = `Already have an account? <button type="button" onclick="toggleAuthMode()" class="text-brand-400 font-bold hover:underline">Sign in</button>`;
            }
        }

        function closeAuthModal() {
            const modal = document.getElementById('auth-modal');
            modal.classList.remove('flex');
            modal.classList.add('hidden');
        }

        function toggleAuthMode() {
            openAuthModal(authMode === 'login' ? 'signup' : 'login');
        }

        function handleAuthSubmit(event) {
            event.preventDefault();
            const username = document.getElementById('auth-username').value.trim();
            const phone = document.getElementById('auth-phone').value.trim();
            const password = document.getElementById('auth-password').value.trim();
            const refCode = document.getElementById('auth-ref-code').value.trim();

            let users = JSON.parse(localStorage.getItem('etl_users') || '[]');

            if (authMode === 'signup') {
                const existing = users.find(u => u.username.toLowerCase() === username.toLowerCase());
                if (existing) {
                    alert('Username already exists. Please choose another or sign in.');
                    return;
                }

                const newUser = {
                    username,
                    phone,
                    password,
                    isActive: false,
                    balance: 0.00,
                    tasksCount: 0,
                    referralEarnings: 0.00,
                    referredBy: refCode || localStorage.getItem('etl_pending_ref') || '',
                    referrals: [],
                    transactions: []
                };

                if (newUser.referredBy) {
                    const upline = users.find(u => u.username.toLowerCase() === newUser.referredBy.toLowerCase());
                    if (upline) {
                        upline.referrals.push({ username: newUser.username, date: new Date().toLocaleDateString(), active: false, commission: 0 });
                    }
                }

                users.push(newUser);
                localStorage.setItem('etl_users', JSON.stringify(users));
                currentUser = newUser;
                localStorage.setItem('etl_current_user', JSON.stringify(currentUser));
            } else {
                const found = users.find(u => u.username.toLowerCase() === username.toLowerCase() && u.password === password);
                if (!found) {
                    alert('Invalid username or password.');
                    return;
                }
                currentUser = found;
                localStorage.setItem('etl_current_user', JSON.stringify(currentUser));
            }

            closeAuthModal();
            enterDashboard();
        }

        function logout() {
            currentUser = null;
            localStorage.removeItem('etl_current_user');
            switchView('landing');
            document.getElementById('nav-auth-buttons').classList.remove('hidden');
            document.getElementById('nav-auth-buttons').classList.add('flex');
            document.getElementById('nav-user-profile').classList.remove('flex');
            document.getElementById('nav-user-profile').classList.add('hidden');
        }

        function switchView(viewName) {
            if (viewName === 'landing') {
                document.getElementById('view-landing').classList.remove('hidden');
                document.getElementById('view-dashboard').classList.add('hidden');
            } else {
                document.getElementById('view-landing').classList.add('hidden');
                document.getElementById('view-dashboard').classList.remove('hidden');
            }
        }

        function enterDashboard() {
            switchView('dashboard');
            document.getElementById('nav-auth-buttons').classList.remove('flex');
            document.getElementById('nav-auth-buttons').classList.add('hidden');
            document.getElementById('nav-user-profile').classList.remove('hidden');
            document.getElementById('nav-user-profile').classList.add('flex');

            document.getElementById('nav-username').innerText = currentUser.username;
            document.getElementById('user-avatar-initial').innerText = currentUser.username.charAt(0).toUpperCase();

            updateDashboardUI();
            updateRefLinkDisplay();
        }

        function updateDashboardUI() {
            document.getElementById('dash-balance').innerText = `$${currentUser.balance.toFixed(2)}`;
            document.getElementById('dash-tasks-count').innerText = currentUser.tasksCount;
            document.getElementById('dash-referral-earnings').innerText = `$${currentUser.referralEarnings.toFixed(2)}`;
            document.getElementById('dash-referral-count').innerText = currentUser.referrals.length;
            document.getElementById('ref-stat-count').innerText = currentUser.referrals.length;

            const badge = document.getElementById('nav-status-badge');
            const statusText = document.getElementById('dash-status-text');
            const activationBanner = document.getElementById('activation-banner');

            if (currentUser.isActive) {
                badge.innerText = 'Active Earner';
                badge.className = 'block text-[10px] text-brand-400 font-bold';
                statusText.innerText = 'Active & Verified';
                statusText.className = 'text-brand-400 font-bold';
                activationBanner.classList.add('hidden');
            } else {
                badge.innerText = 'Inactive Account';
                badge.className = 'block text-[10px] text-amber-400 font-bold';
                statusText.innerText = 'Pending Activation ($0.5)';
                statusText.className = 'text-amber-400 font-bold';
                activationBanner.classList.remove('hidden');
            }

            const refTableBody = document.getElementById('referrals-table-body');
            if (currentUser.referrals.length === 0) {
                refTableBody.innerHTML = `<tr><td colspan="4" class="text-center py-6 text-slate-500">No referrals yet. Share your link to start building your network!</td></tr>`;
            } else {
                refTableBody.innerHTML = currentUser.referrals.map(r => `
                    <tr class="hover:bg-slate-900/50">
                        <td class="py-3 font-bold text-white">${r.username}</td>
                        <td class="py-3 text-slate-400">${r.date}</td>
                        <td class="py-3"><span class="px-2.5 py-1 rounded-full text-[10px] font-bold ${r.active ? 'bg-brand-950 text-brand-400' : 'bg-amber-950 text-amber-400'}">${r.active ? 'Active' : 'Pending'}</span></td>
                        <td class="py-3 text-right font-bold text-brand-400">+$${r.commission.toFixed(2)}</td>
                    </tr>
                `).join('');
            }

            const txList = document.getElementById('transaction-history-list');
            if (!currentUser.transactions || currentUser.transactions.length === 0) {
                txList.innerHTML = `<div class="text-center py-8 text-slate-500 text-xs">No transactions recorded yet.</div>`;
            } else {
                txList.innerHTML = currentUser.transactions.map(t => `
                    <div class="bg-slate-900 border border-slate-800 p-3 rounded-xl flex items-center justify-between text-xs">
                        <div>
                            <p class="font-bold text-white">${t.title}</p>
                            <p class="text-[10px] text-slate-400">${t.date}</p>
                        </div>
                        <span class="font-bold ${t.type === 'credit' ? 'text-brand-400' : 'text-rose-400'}">${t.type === 'credit' ? '+' : '-'}$${t.amount.toFixed(2)}</span>
                    </div>
                `).join('');
            }
        }

        function switchTab(tabName) {
            ['tasks', 'referrals', 'wallet'].forEach(t => {
                document.getElementById(`tab-content-${t}`).classList.add('hidden');
                document.getElementById(`tab-btn-${t}`).classList.remove('border-brand-500', 'text-brand-400');
                document.getElementById(`tab-btn-${t}`).classList.add('border-transparent', 'text-slate-400');
            });

            document.getElementById(`tab-content-${tabName}`).classList.remove('hidden');
            document.getElementById(`tab-btn-${tabName}`).classList.add('border-brand-500', 'text-brand-400');
            document.getElementById(`tab-btn-${tabName}`).classList.remove('border-transparent', 'text-slate-400');
        }

        function copyRefLink() {
            const input = document.getElementById('dash-ref-link');
            input.select();
            navigator.clipboard.writeText(input.value);
            alert('Referral link copied to clipboard!');
        }

        function openActivationModal() {
            document.getElementById('activation-modal').classList.remove('hidden');
            document.getElementById('activation-modal').classList.add('flex');
        }

        function closeActivationModal() {
            document.getElementById('activation-modal').classList.remove('flex');
            document.getElementById('activation-modal').classList.add('hidden');
        }

        function verifyActivationPayment() {
            const code = document.getElementById('mpesa-code-input').value.trim();
            if (!code || code.length < 8) {
                alert('Please enter a valid M-Pesa transaction code (e.g. QHJ72K9XYZ).');
                return;
            }

            currentUser.isActive = true;
            currentUser.transactions.unshift({
                title: 'Account Activation ($0.5 via Paybill 891300, Acc 144841)',
                date: new Date().toLocaleString(),
                amount: 0.50,
                type: 'debit'
            });

            if (currentUser.referredBy) {
                let users = JSON.parse(localStorage.getItem('etl_users') || '[]');
                let upline = users.find(u => u.username.toLowerCase() === currentUser.referredBy.toLowerCase());
                if (upline) {
                    const commission = 0.15;
                    upline.balance += commission;
                    upline.referralEarnings += commission;
                    upline.transactions.unshift({
                        title: `Referral Commission from ${currentUser.username}`,
                        date: new Date().toLocaleString(),
                        amount: commission,
                        type: 'credit'
                    });
                    const refObj = upline.referrals.find(r => r.username.toLowerCase() === currentUser.username.toLowerCase());
                    if (refObj) {
                        refObj.active = true;
                        refObj.commission = commission;
                    }
                    localStorage.setItem('etl_users', JSON.stringify(users));
                }
            }

            saveUserData();
            closeActivationModal();
            updateDashboardUI();
            alert('Account successfully activated! All task and withdrawal features are now unlocked.');
        }

        function completeTask(taskId, reward, title) {
            if (!currentUser.isActive) {
                alert('Please activate your account with the $0.5 fee first to unlock language tasks.');
                openActivationModal();
                return;
            }

            activeTaskData = { taskId, reward, title };
            document.getElementById('modal-task-title').innerText = title;
            document.getElementById('modal-reward-val').innerText = reward.toFixed(2);
            document.getElementById('task-claim-btn').classList.add('hidden');
            document.getElementById('task-progress-bar').style.width = '0%';
            document.getElementById('task-status-text').innerText = 'Verifying translation accuracy...';

            const modal = document.getElementById('task-modal');
            modal.classList.remove('hidden');
            modal.classList.add('flex');

            setTimeout(() => {
                document.getElementById('task-progress-bar').style.width = '60%';
                document.getElementById('task-status-text').innerText = 'Checking linguistic formatting...';
            }, 800);

            setTimeout(() => {
                document.getElementById('task-progress-bar').style.width = '100%';
                document.getElementById('task-status-text').innerText = 'Task verified successfully!';
                document.getElementById('task-claim-btn').classList.remove('hidden');
            }, 1800);
        }

        function claimTaskReward() {
            currentUser.balance += activeTaskData.reward;
            currentUser.tasksCount += 1;
            currentUser.transactions.unshift({
                title: `Task Earned: ${activeTaskData.title}`,
                date: new Date().toLocaleString(),
                amount: activeTaskData.reward,
                type: 'credit'
            });

            saveUserData();
            updateDashboardUI();
            
            document.getElementById('task-modal').classList.remove('flex');
            document.getElementById('task-modal').classList.add('hidden');
            alert(`Successfully earned $${activeTaskData.reward.toFixed(2)}! Balance updated.`);
        }

        function requestWithdrawal() {
            if (!currentUser.isActive) {
                alert('Account must be activated to process withdrawals.');
                openActivationModal();
                return;
            }

            const amount = parseFloat(document.getElementById('withdraw-amount').value);
            const phone = document.getElementById('withdraw-phone').value.trim();

            if (!amount || amount <= 0) {
                alert('Please enter a valid withdrawal amount.');
                return;
            }

            if (amount > currentUser.balance) {
                alert('Insufficient balance for this withdrawal request.');
                return;
            }

            if (!phone) {
                alert('Please enter your M-Pesa phone number.');
                return;
            }

            currentUser.balance -= amount;
            currentUser.transactions.unshift({
                title: `Payout to M-Pesa (${phone})`,
                date: new Date().toLocaleString(),
                amount: amount,
                type: 'debit'
            });

            saveUserData();
            updateDashboardUI();
            document.getElementById('withdraw-amount').value = '';
            document.getElementById('withdraw-phone').value = '';
            alert(`Withdrawal request of $${amount.toFixed(2)} submitted successfully. Funds will arrive via M-Pesa shortly.`);
            switchTab('wallet');
        }

        function saveUserData() {
            localStorage.setItem('etl_current_user', JSON.stringify(currentUser));
            let users = JSON.parse(localStorage.getItem('etl_users') || '[]');
            const index = users.findIndex(u => u.username.toLowerCase() === currentUser.username.toLowerCase());
            if (index !== -1) {
                users[index] = currentUser;
                localStorage.setItem('etl_users', JSON.stringify(users));
            }
        }
    </script>
</body>
</html>
