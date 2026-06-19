<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Volley Club — Premium Pickleball Bookings</title>
    <!-- Tailwind CSS for Styling -->
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
</head>
<body class="bg-[#FAF9F5] text-[#1C2D27] font-sans antialiased">

    <div id="top" class="min-h-screen bg-[#FAF9F5] text-[#1C2D27]">
        
        <!-- SUCCESS TOAST -->
        <div id="successToast" class="hidden fixed bottom-6 right-6 z-50 max-w-md bg-[#1C2D27] text-[#FAF9F5] p-5 rounded-2xl shadow-2xl border border-lime-400/30 flex items-start gap-4">
            <div class="text-lime-400 text-xl font-bold">✓</div>
            <div>
                <h4 class="font-bold text-lg text-white">Reservation Submitted!</h4>
                <p class="text-sm text-[#FAF9F5]/80 mt-1">
                    A confirmation request has been dispatched to management at <span class="text-lime-400 font-medium">marcjoseph.igs@gmail.com</span>.
                </p>
            </div>
        </div>

        <!-- HEADER -->
        <header class="sticky top-0 z-40 bg-[#FAF9F5]/90 backdrop-blur-md border-b border-[#1C2D27]/5">
            <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
                <a href="#top" class="flex items-center gap-2 font-black text-2xl tracking-tight text-[#1C2D27]">
                    <span class="w-3 h-3 bg-lime-400 rounded-full inline-block"></span>
                    Volley Club
                </a>
                <nav class="hidden md:flex items-center gap-8 font-semibold text-sm tracking-wide text-[#1C2D27]/80">
                    <a href="#book" class="hover:text-[#1C2D27] transition-colors">Book</a>
                    <a href="#contact" class="hover:text-[#1C2D27] transition-colors">Contact</a>
                </nav>
                <a href="#book" class="bg-[#1C2D27] text-white hover:bg-[#253B33] px-5 py-2.5 rounded-full font-bold text-sm transition-all shadow-sm">
                    Book a Court
                </a>
            </div>
        </header>

        <!-- HERO -->
        <section class="max-w-7xl mx-auto px-6 py-12 lg:py-24 grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
            <div class="lg:col-span-7 space-y-8">
                <span class="inline-flex items-center gap-2 bg-[#1C2D27]/5 px-4 py-1.5 rounded-full text-xs font-bold uppercase tracking-wider text-[#1C2D27]">
                    <span class="w-1.5 h-1.5 bg-[#1C2D27] rounded-full"></span>
                    Now booking — Summer season
                </span>
                <h1 class="text-5xl lg:text-7xl font-black tracking-tighter leading-none text-[#1C2D27]">
                    Your court.<br />Your time.<br /><span class="text-[#1C2D27]/40">Your game.</span>
                </h1>
                <p class="text-lg lg:text-xl text-[#1C2D27]/70 font-normal max-w-xl leading-relaxed">
                    Welcome, player. Reserve a premium pickleball court in under a minute — pro surfaces, perfect lighting, and gear ready when you arrive.
                </p>
                <div class="flex flex-wrap items-center gap-4 pt-2">
                    <a href="#book" class="bg-[#1C2D27] text-white hover:bg-[#253B33] px-8 py-4 rounded-full font-bold text-base transition-all shadow-md">
                        Book a Court
                    </a>
                </div>
            </div>
            
            <div class="lg:col-span-5 relative">
                <div class="rounded-3xl overflow-hidden shadow-2xl relative aspect-[4/3] bg-emerald-900/30">
                    <div class="absolute inset-0 bg-gradient-to-t from-[#1C2D27]/80 via-transparent to-transparent z-10"></div>
                    <div class="absolute inset-0 bg-cover bg-center mix-blend-overlay" style="background-image: url('https://images.unsplash.com/photo-1626224583764-f87db24ac4ea?auto=format&fit=crop&q=80&w=1000')"></div>
                    <div class="absolute bottom-6 left-6 z-20 text-white">
                        <div class="text-xs uppercase font-bold tracking-widest text-lime-400 mb-1">Featured court</div>
                        <div class="text-xl font-bold">Center Court · Indoor</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- BOOKING SECTION -->
        <section id="book" class="bg-white border-y border-[#1C2D27]/5 py-20">
            <div class="max-w-7xl mx-auto px-6">
                <div class="mb-12 max-w-xl">
                    <span class="text-xs uppercase font-black tracking-widest text-[#1C2D27]/50">Booking engine</span>
                    <h2 class="text-3xl lg:text-5xl font-black tracking-tight text-[#1C2D27] mt-2">Reserve your court.</h2>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-start">
                    <div class="lg:col-span-8 space-y-10">
                        <!-- Date Selection -->
                        <div class="space-y-4">
                            <h3 class="font-bold text-lg text-[#1C2D27]">01. Select a date</h3>
                            <div class="grid grid-cols-5 gap-3" id="dateGroup">
                                <button onclick="selectDate('Wed, Jun 10')" class="date-btn p-4 rounded-2xl flex flex-col items-center justify-center border transition-all bg-[#1C2D27] text-white">
                                    <span class="text-xs opacity-60 uppercase mb-1">Wed</span><span class="text-xl font-black">10</span>
                                </button>
                                <button onclick="selectDate('Thu, Jun 11')" class="date-btn p-4 rounded-2xl flex flex-col items-center justify-center border transition-all border-[#1C2D27]/10 bg-white text-[#1C2D27]">
                                    <span class="text-xs opacity-60 uppercase mb-1">Thu</span><span class="text-xl font-black">11</span>
                                </button>
                                <button onclick="selectDate('Fri, Jun 12')" class="date-btn p-4 rounded-2xl flex flex-col items-center justify-center border transition-all border-[#1C2D27]/10 bg-white text-[#1C2D27]">
                                    <span class="text-xs opacity-60 uppercase mb-1">Fri</span><span class="text-xl font-black">12</span>
                                </button>
                                <button onclick="selectDate('Sat, Jun 13')" class="date-btn p-4 rounded-2xl flex flex-col items-center justify-center border transition-all border-[#1C2D27]/10 bg-white text-[#1C2D27]">
                                    <span class="text-xs opacity-60 uppercase mb-1">Sat</span><span class="text-xl font-black">13</span>
                                </button>
                                <button onclick="selectDate('Sun, Jun 14')" class="date-btn p-4 rounded-2xl flex flex-col items-center justify-center border transition-all border-[#1C2D27]/10 bg-white text-[#1C2D27]">
                                    <span class="text-xs opacity-60 uppercase mb-1">Sun</span><span class="text-xl font-black">14</span>
                                </button>
                            </div>
                        </div>

                        <!-- Court Selection -->
                        <div class="space-y-4">
                            <h3 class="font-bold text-lg text-[#1C2D27]">02. Select a court</h3>
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-4" id="courtGroup">
                                <button onclick="selectCourt('Court 1', 'Pro cushioning, premium climate control')" class="court-btn p-5 rounded-2xl text-left border transition-all bg-[#1C2D27] text-white">
                                    <div class="font-bold text-base">Court 1</div>
                                    <div class="text-xs opacity-70 mt-2">Pro cushioning, premium climate control</div>
                                </button>
                                <button onclick="selectCourt('Court 2', 'Clear views, professional court surfacing')" class="court-btn p-5 rounded-2xl text-left border transition-all border-[#1C2D27]/10 bg-white text-[#1C2D27]">
                                    <div class="font-bold text-base">Court 2</div>
                                    <div class="text-xs opacity-70 mt-2">Clear views, professional court surfacing</div>
                                </button>
                            </div>
                        </div>

                        <!-- Time Selection -->
                        <div class="space-y-4">
                            <h3 class="font-bold text-lg text-[#1C2D27]">03. Available times</h3>
                            <div class="grid grid-cols-2 sm:grid-cols-5 gap-3" id="timeGroup">
                                <button onclick="selectTime(this, '08:00 AM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">08:00 AM</button>
                                <button onclick="selectTime(this, '09:00 AM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">09:00 AM</button>
                                <button onclick="selectTime(this, '10:00 AM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">10:00 AM</button>
                                <button onclick="selectTime(this, '11:00 AM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">11:00 AM</button>
                                <button onclick="selectTime(this, '01:00 PM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">01:00 PM</button>
                                <button onclick="selectTime(this, '02:00 PM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">02:00 PM</button>
                                <button onclick="selectTime(this, '03:00 PM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">03:00 PM</button>
                                <button onclick="selectTime(this, '04:00 PM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">04:00 PM</button>
                                <button onclick="selectTime(this, '05:00 PM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">05:00 PM</button>
                                <button onclick="selectTime(this, '06:00 PM')" class="time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white">06:00 PM</button>
                            </div>
                        </div>

                        <!-- Add-ons -->
                        <div class="space-y-4">
                            <h3 class="font-bold text-lg text-[#1C2D27]">04. Gear Add-ons</h3>
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                <div class="p-5 border border-[#1C2D27]/10 rounded-2xl flex items-center justify-between">
                                    <div>
                                        <div class="font-bold">Paddle rental</div>
                                        <div class="text-xs opacity-60">$8.00 each</div>
                                    </div>
                                    <div class="flex items-center gap-3">
                                        <button onclick="updateAddon('paddles', -1)" class="px-2 bg-gray-100 rounded">-</button>
                                        <span id="paddleCount" class="font-bold">0</span>
                                        <button onclick="updateAddon('paddles', 1)" class="px-2 bg-gray-100 rounded">+</button>
                                    </div>
                                </div>
                                <div class="p-5 border border-[#1C2D27]/10 rounded-2xl flex items-center justify-between">
                                    <div>
                                        <div class="font-bold">Pickleballs (3-pack)</div>
                                        <div class="text-xs opacity-60">$5.00 each</div>
                                    </div>
                                    <div class="flex items-center gap-3">
                                        <button onclick="updateAddon('balls', -1)" class="px-2 bg-gray-100 rounded">-</button>
                                        <span id="ballCount" class="font-bold">0</span>
                                        <button onclick="updateAddon('balls', 1)" class="px-2 bg-gray-100 rounded">+</button>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- SIDEBAR -->
                    <div class="lg:col-span-4 bg-[#1C2D27] text-white p-6 rounded-3xl space-y-6 shadow-xl">
                        <h3 class="text-xl font-black tracking-tight">Your reservation</h3>
                        <div class="space-y-3 text-sm border-t border-b border-white/10 py-4">
                            <div class="flex justify-between"><span>Date</span><span id="summaryDate">Wed, Jun 10</span></div>
                            <div class="flex justify-between"><span>Court</span><span id="summaryCourt" class="truncate max-w-[150px]">Court 1</span></div>
                            <div class="flex justify-between"><span>Time</span><span id="summaryTime" class="text-lime-400 font-bold">—</span></div>
                            <div class="flex justify-between text-xs opacity-60"><span>Court Fee</span><span>$45.00</span></div>
                        </div>
                        <div class="flex justify-between items-baseline">
                            <span class="font-bold">Total</span>
                            <span class="text-3xl font-black text-lime-400" id="summaryTotal">$45.00</span>
                        </div>
                        <button onclick="handleBookNow()" class="w-full bg-lime-400 text-[#1C2D27] py-4 rounded-xl font-black tracking-wide text-center hover:bg-lime-300 transition-colors cursor-pointer">
                            Book Now
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- CONTACT PANEL -->
        <section id="contact" class="bg-[#1C2D27] text-white py-20 text-center">
            <div class="max-w-4xl mx-auto px-6 space-y-6">
                <h2 class="text-3xl lg:text-5xl font-black">Ready to play? Connect with us.</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-4 pt-6 max-w-3xl mx-auto text-left">
                    <a href="mailto:marcjoseph.igs@gmail.com" class="bg-white/5 border border-white/10 p-5 rounded-2xl flex flex-col gap-1">
                        <span class="text-xs opacity-50 uppercase font-bold">Email</span>
                        <span class="text-sm font-bold truncate">marcjoseph.igs@gmail.com</span>
                    </a>
                    <a href="tel:+639750438933" class="bg-white/5 border border-white/10 p-5 rounded-2xl flex flex-col gap-1">
                        <span class="text-xs opacity-50 uppercase font-bold">Call us</span>
                        <span class="text-sm font-bold">+63 975 043 8933</span>
                    </a>
                    <a href="https://wa.me/639750438933" target="_blank" class="bg-white/5 border border-white/10 p-5 rounded-2xl flex flex-col gap-1">
                        <span class="text-xs opacity-50 uppercase font-bold">WhatsApp</span>
                        <span class="text-sm font-bold text-lime-400">Chat Instantly</span>
                    </a>
                </div>
            </div>
        </section>
    </div>

    <!-- NATIVE JAVASCRIPT STATE ENGINE -->
    <script>
        let state = {
            date: 'Wed, Jun 10',
            court: 'Court 1',
            time: '',
            paddles: 0,
            balls: 0,
            courtFee: 45.00,
            paddlePrice: 8.00,
            ballPrice: 5.00
        };

        function selectDate(dateVal) {
            state.date = dateVal;
            document.getElementById('summaryDate').innerText = dateVal;
            
            const buttons = document.querySelectorAll('.date-btn');
            buttons.forEach(btn => {
                if(btn.outerHTML.includes(dateVal)) {
                    btn.className = "date-btn p-4 rounded-2xl flex flex-col items-center justify-center border transition-all bg-[#1C2D27] text-white";
                } else {
                    btn.className = "date-btn p-4 rounded-2xl flex flex-col items-center justify-center border transition-all border-[#1C2D27]/10 bg-white text-[#1C2D27]";
                }
            });
        }

        function selectCourt(courtName, details) {
            state.court = courtName;
            document.getElementById('summaryCourt').innerText = courtName;

            const buttons = document.querySelectorAll('.court-btn');
            buttons.forEach(btn => {
                if(btn.querySelector('.text-base').innerText === courtName) {
                    btn.className = "court-btn p-5 rounded-2xl text-left border transition-all bg-[#1C2D27] text-white";
                } else {
                    btn.className = "court-btn p-5 rounded-2xl text-left border transition-all border-[#1C2D27]/10 bg-white text-[#1C2D27]";
                }
            });
        }

        function selectTime(element, timeVal) {
            state.time = timeVal;
            document.getElementById('summaryTime').innerText = timeVal;

            const buttons = document.querySelectorAll('.time-btn');
            buttons.forEach(btn => {
                btn.className = "time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all border-[#1C2D27]/10 bg-white";
            });
            element.className = "time-btn py-3 px-4 rounded-xl font-bold text-sm text-center border transition-all bg-lime-400 text-[#1C2D27]";
        }

        function updateAddon(type, amount) {
            if (type === 'paddles') {
                state.paddles = Math.max(0, state.paddles + amount);
                document.getElementById('paddleCount').innerText = state.paddles;
            } else if (type === 'balls') {
                state.balls = Math.max(0, state.balls + amount);
                document.getElementById('ballCount').innerText = state.balls;
            }
            calculateTotal();
        }

        function calculateTotal() {
            let total = state.courtFee + (state.paddles * state.paddlePrice) + (state.balls * state.ballPrice);
            document.getElementById('summaryTotal').innerText = `$${total.toFixed(2)}`;
        }

        function handleBookNow() {
            if (!state.time) {
                alert("Please select an available time slot before finalizing your reservation.");
                return;
            }
            const toast = document.getElementById('successToast');
            toast.classList.remove('hidden');
            setTimeout(() => {
                toast.classList.add('hidden');
            }, 6000);
        }
    </script>
</body>
</html>
