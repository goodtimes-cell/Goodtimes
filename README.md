<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Good Times Radio - Live Streaming</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f8f9fa;
            color: #333;
            overflow-x: hidden;
        }
        
        .gradient-bg {
            background: linear-gradient(135deg, #6e45e2 0%, #88d3ce 100%);
        }
        
        .player-progress {
            height: 6px;
            width: 100%;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 3px;
            cursor: pointer;
        }
        
        .player-progress-filled {
            height: 100%;
            width: 0%;
            background: linear-gradient(90deg, #ff9a9e 0%, #fad0c4 100%);
            border-radius: 3px;
            transition: width 0.1s linear;
        }
        
        .social-icon {
            transition: all 0.3s ease;
        }
        
        .social-icon:hover {
            transform: translateY(-5px);
            filter: drop-shadow(0 5px 5px rgba(0, 0, 0, 0.2));
        }
        
        .now-playing-image {
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }
        
        .stream-platform {
            transition: all 0.3s ease;
            border: 2px solid transparent;
        }
        
        .stream-platform:hover {
            transform: scale(1.05);
            border-color: rgba(255, 255, 255, 0.5);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }
        
        .card-glass {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 10px;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .schedule-item:not(:last-child) {
            border-bottom: 1px solid rgba(255, 255, 255, 0.2);
        }
    </style>
</head>
<body class="gradient-bg min-h-screen text-white">
    <!-- Header -->
    <header class="pt-6 pb-2 px-4 md:px-8 lg:px-12">
        <div class="container mx-auto flex flex-col md:flex-row justify-between items-center">
            <div class="flex items-center mb-4 md:mb-0">
                <i class="fas fa-broadcast-tower text-3xl mr-3 text-yellow-300"></i>
                <h1 class="text-2xl md:text-3xl font-bold tracking-wider">GOOD TIMES RADIO</h1>
            </div>
            <nav class="flex space-x-4 md:space-x-6">
                <a href="#" class="hover:text-yellow-300 transition">Home</a>
                <a href="#live" class="hover:text-yellow-300 transition">Live</a>
                <a href="#schedule" class="hover:text-yellow-300 transition">Schedule</a>
                <a href="#about" class="hover:text-yellow-300 transition">About</a>
                <a href="#contact" class="hover:text-yellow-300 transition">Contact</a>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="py-12 md:py-20 px-4 md:px-8 lg:px-12">
        <div class="container mx-auto flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-10 md:mb-0">
                <h2 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
                    Feel the <span class="text-yellow-300">Good Vibes</span> with Our Music
                </h2>
                <p class="text-lg md:text-xl mb-8 opacity-90">
                    Tune in to Good Times Radio for the best music selection, live shows, and entertainment. Streaming 24/7 to make your days better.
                </p>
                <div class="flex space-x-4">
                    <a href="#live" class="bg-yellow-400 hover:bg-yellow-500 text-gray-900 px-6 py-3 rounded-lg font-medium transition transform hover:scale-105">
                        <i class="fas fa-play mr-2"></i> Listen Live
                    </a>
                    <a href="#" class="border-2 border-white hover:bg-white hover:text-gray-900 px-6 py-3 rounded-lg font-medium transition">
                        Become a Member
                    </a>
                </div>
            </div>
            <div class="md:w-1/2 flex justify-center">
                <img src="https://images.unsplash.com/photo-1571330735066-03aaa9429d89?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                     alt="Radio Studio" 
                     class="rounded-2xl shadow-2xl w-full max-w-md now-playing-image">
            </div>
        </div>
    </section>

    <!-- Live Streaming Section -->
    <section id="live" class="py-12 px-4 md:px-8 lg:px-12 bg-black bg-opacity-20">
        <div class="container mx-auto">
            <h2 class="text-3xl md:text-4xl font-bold mb-8 text-center">
                <i class="fas fa-signal mr-2 text-yellow-300"></i> Live Streaming Now
            </h2>
            
            <!-- Player -->
            <div class="card-glass p-6 md:p-8 rounded-xl max-w-4xl mx-auto mb-12">
                <div class="flex flex-col md:flex-row items-center mb-6">
                    <img src="https://images.unsplash.com/photo-1470225620780-dba8ba36b745?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                         alt="Now Playing" 
                         class="w-24 h-24 md:w-32 md:h-32 rounded-lg object-cover mr-6 mb-4 md:mb-0 shadow-lg">
                    
                    <div class="flex-1">
                        <h3 class="text-xl font-bold mb-1">Live Mix: Summer Vibes</h3>
                        <p class="opacity-80 mb-3">DJ Mario Sunshine • Playing Now</p>
                        
                        <div class="player-progress mb-3">
                            <div class="player-progress-filled"></div>
                        </div>
                        
                        <div class="flex justify-between text-sm opacity-80 mb-4">
                            <span id="current-time">00:00</span>
                            <span id="duration">03:24</span>
                        </div>
                        
                        <div class="flex justify-between items-center">
                            <button class="player-control hover:text-yellow-300 transition">
                                <i class="fas fa-backward text-2xl"></i>
                            </button>
                            <button id="play-btn" class="bg-yellow-400 hover:bg-yellow-500 text-gray-900 rounded-full w-14 h-14 flex items-center justify-center transition transform hover:scale-105">
                                <i class="fas fa-play text-2xl"></i>
                            </button>
                            <button class="player-control hover:text-yellow-300 transition">
                                <i class="fas fa-forward text-2xl"></i>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Streaming Platforms -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-8">
                <div class="stream-platform bg-red-600 hover:bg-red-700 p-6 rounded-xl flex flex-col items-center justify-center text-center cursor-pointer transition">
                    <i class="fab fa-youtube text-5xl mb-4"></i>
                    <h3 class="text-xl font-bold mb-2">YouTube Live</h3>
                    <p class="opacity-90 mb-4">Watch our live video stream on YouTube</p>
                    <a href="#" class="bg-black hover:bg-gray-900 text-white px-4 py-2 rounded-full transition">
                        Watch Now
                    </a>
                </div>
                
                <div class="stream-platform bg-blue-700 hover:bg-blue-800 p-6 rounded-xl flex flex-col items-center justify-center text-center cursor-pointer transition">
                    <i class="fab fa-facebook text-5xl mb-4"></i>
                    <h3 class="text-xl font-bold mb-2">Facebook Live</h3>
                    <p class="opacity-90 mb-4">Connect with us on Facebook Live</p>
                    <a href="#" class="bg-black hover:bg-gray-900 text-white px-4 py-2 rounded-full transition">
                        Join Live
                    </a>
                </div>
                
                <div class="stream-platform bg-gray-900 hover:bg-black p-6 rounded-xl flex flex-col items-center justify-center text-center cursor-pointer transition">
                    <i class="fas fa-microphone-alt text-5xl mb-4"></i>
                    <h3 class="text-xl font-bold mb-2">Audio Stream</h3>
                    <p class="opacity-90 mb-4">Just want the audio? Click here</p>
                    <a href="#" class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-full transition">
                        Listen Now
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Schedule Section -->
    <section id="schedule" class="py-12 px-4 md:px-8 lg:px-12 bg-black bg-opacity-20">
        <div class="container mx-auto">
            <h2 class="text-3xl md:text-4xl font-bold mb-8 text-center">
                <i class="far fa-calendar-alt mr-2 text-yellow-300"></i> Weekly Schedule
            </h2>
            
            <div class="card-glass p-6 rounded-2xl max-w-4xl mx-auto">
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                    <!-- Monday Schedule -->
                    <div class="schedule-day">
                        <h3 class="text-xl font-bold mb-4 flex items-center">
                            <i class="far fa-sun mr-2 text-yellow-300"></i> Monday
                        </h3>
                        <div class="space-y-3">
                            <div class="schedule-item pb-3">
                                <div class="flex justify-between">
                                    <span class="font-medium">Morning Mix</span>
                                    <span class="opacity-80">6:00 - 10:00</span>
                                </div>
                                <p class="text-sm opacity-70 mt-1">DJ Anna Sunrise</p>
                            </div>
                            <div class="schedule-item pb-3">
                                <div class="flex justify-between">
                                    <span class="font-medium">Pop Hits</span>
                                    <span class="opacity-80">12:00 - 15:00</span>
                                </div>
                                <p class="text-sm opacity-70 mt-1">DJ Mike</p>
                            </div>
                            <div class="schedule-item pb-3">
                                <div class="flex justify-between">
                                    <span class="font-medium">Chill Vibes</span>
                                    <span class="opacity-80">18:00 - 21:00</span>
                                </div>
                                <p class="text-sm opacity-70 mt-1">DJ Clara</p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Wednesday Schedule -->
                    <div class="schedule-day">
                        <h3 class="text-xl font-bold mb-4 flex items-center">
                            <i class="far fa-sun mr-2 text-yellow-300"></i> Wednesday
                        </h3>
                        <div class="space-y-3">
                            <div class="schedule-item pb-3">
                                <div class="flex justify-between">
                                    <span class="font-medium">Wake Up Show</span>
                                    <span class="opacity-80">6:00 - 10:00</span>
                                </div>
                                <p class="text-sm opacity-70 mt-1">DJ Mark</p>
                            </div>
                            <div class="schedule-item pb-3">
                                <div class="flex justify-between">
                                    <span class="font-medium">Rock Zone</span>
                                    <span class="opacity-80">12:00 - 15:00</span>
                                </div>
                                <p class="text-sm opacity-70 mt-1">DJ Steve</p>
                            </div>
                            <div class="schedule-item pb-3">
                                <div class="flex justify-between">
                                    <span class="font-medium">Latin Nights</span>
                                    <span class="opacity-80">18:00 - 21:00</span>
                                </div>
                                <p class="text-sm opacity-70 mt-1">DJ Carlos</p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Friday Schedule -->
                    <div class="schedule-day">
                        <h3 class="text-xl font-bold mb-4 flex items-center">
                            <i class="far fa-sun mr-2 text-yellow-300"></i> Friday
                        </h3>
                        <div class="space-y-3">
                            <div class="schedule-item pb-3">
                                <div class="flex justify-between">
                                    <span class="font-medium">Friday Morning</span>
                                    <span class="opacity-80">6:00 - 10:00</span>
                                </div>
                                <p class="text-sm opacity-70 mt-1">DJ Anna & DJ Mike</p>
                            </div>
                            <div class="schedule-item pb-3">
                                <div class="flex justify-between">
                                    <span class="font-medium">Freestyle Show</span>
                                    <span class="opacity-80">12:00 - 15:00</span>
                                </div>
                                <p class="text-sm opacity-70 mt-1">DJ Flex</p>
                            </div>
                            <div class="schedule-item pb-3">
                                <div class="flex justify-between">
                                    <span class="font-medium">Weekend Party</span>
                                    <span class="opacity-80">18:00 - 00:00</span>
                                </div>
                                <p class="text-sm opacity-70 mt-1">DJ Party Crew</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- View Full Schedule Button -->
                <div class="text-center mt-8">
                    <a href="#" class="border-2 border-white hover:bg-white hover:text-gray-900 px-6 py-3 rounded-lg font-medium inline-block transition transform hover:scale-105">
                        <i class="far fa-calendar-check mr-2"></i> View Full Schedule
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-12 px-4 md:px-8 lg:px-12">
        <div class="container mx-auto">
            <h2 class="text-3xl md:text-4xl font-bold mb-8 text-center">
                <i class="fas fa-info-circle mr-2 text-yellow-300"></i> About Good Times Radio
            </h2>
            
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0 md:pr-8">
                    <img src="https://images.unsplash.com/photo-1511671782779-c97d3d27a1d4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" 
                         alt="Radio Studio" 
                         class="rounded-xl shadow-xl w-full">
                </div>
                
                <div class="md:w-1/2">
                    <h3 class="text-2xl font-bold mb-4">Bringing Good Times Since 2010</h3>
                    <p class="mb-4 opacity-90">
                        Good Times Radio was founded with one simple mission: to spread joy through music. Our
