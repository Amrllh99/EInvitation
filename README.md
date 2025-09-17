<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Ava & Noah — Wedding Invitation</title>

  <!-- Tailwind CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            blossom: {
              50: '#fff8fb',
              100: '#ffeff6',
              200: '#ffd7e8',
              300: '#ffb7d4',
              400: '#ff8fbb',
              500: '#ff68a3',
              600: '#e64a89',
              700: '#c53571',
              800: '#9e2b5c',
              900: '#7f274d'
            },
            forest: {
              50: '#f3fbf6',
              100: '#e5f6ec',
              200: '#c6ecd8',
              300: '#97dbba',
              400: '#5ac294',
              500: '#2aa272',
              600: '#1d855d',
              700: '#186a4c',
              800: '#155540',
              900: '#124636'
            }
          },
          fontFamily: {
            display: ['"Playfair Display"', 'serif'],
            sans: ['Inter', 'ui-sans-serif', 'system-ui', 'sans-serif'],
            script: ['"Great Vibes"', 'cursive']
          },
          boxShadow: {
            soft: '0 10px 30px rgba(0,0,0,0.12)'
          },
          backgroundImage: {
            'botanical': 'radial-gradient(1200px 600px at 10% -10%, rgba(255,255,255,0.25) 0%, transparent 60%), radial-gradient(1000px 600px at 110% 10%, rgba(255,255,255,0.22) 0%, transparent 55%), linear-gradient(120deg, #2aa272 0%, #ff68a3 100%)'
          }
        }
      }
    }
  </script>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Inter:wght@300;400;600&family=Playfair+Display:wght@400;600;700&display=swap" rel="stylesheet">

  <style>
    /* Subtle grain for depth */
    .grain:before {
      content: "";
      position: absolute;
      inset: 0;
      background-image: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" opacity="0.045" width="120" height="120" viewBox="0 0 120 120"><filter id="n"><feTurbulence type="fractalNoise" baseFrequency="0.9" numOctaves="2" stitchTiles="stitch"/></filter><rect width="100%" height="100%" filter="url(%23n)"/></svg>');
      pointer-events: none;
      mix-blend-mode: overlay;
    }
    /* Floating petals animation */
    @keyframes float {
      0% { transform: translateY(0) translateX(0) rotate(0deg); opacity: 0.8; }
      50% { transform: translateY(-20px) translateX(10px) rotate(6deg); opacity: 1; }
      100% { transform: translateY(0) translateX(0) rotate(0deg); opacity: 0.85; }
    }
    .petal {
      animation: float 6s ease-in-out infinite;
    }
    /* Smooth section reveal */
    .reveal {
      opacity: 0;
      transform: translateY(12px);
      transition: opacity .6s ease, transform .6s ease;
    }
    .reveal.show {
      opacity: 1;
      transform: translateY(0);
    }
  </style>
</head>

<body class="min-h-screen bg-botanical relative overflow-x-hidden">
  <!-- Decorative corner foliage (SVG, no external images) -->
  <div class="pointer-events-none absolute -top-6 -left-6 opacity-30">
    <svg width="220" height="220" viewBox="0 0 200 200" fill="none">
      <path d="M20 160 C80 120, 40 80, 120 40" stroke="#ffffff" stroke-opacity="0.7" stroke-width="2" />
      <path d="M30 150 C90 110, 60 70, 130 30" stroke="#ffffff" stroke-opacity="0.5" stroke-width="2" />
      <circle cx="120" cy="40" r="6" fill="#ffffff" fill-opacity="0.7"/>
      <circle cx="130" cy="30" r="4" fill="#ffffff" fill-opacity="0.6"/>
    </svg>
  </div>
  <div class="pointer-events-none absolute -bottom-10 -right-10 opacity-30 rotate-180">
    <svg width="260" height="260" viewBox="0 0 200 200" fill="none">
      <path d="M20 160 C80 120, 40 80, 120 40" stroke="#ffffff" stroke-opacity="0.7" stroke-width="2" />
      <path d="M30 150 C90 110, 60 70, 130 30" stroke="#ffffff" stroke-opacity="0.5" stroke-width="2" />
      <circle cx="120" cy="40" r="6" fill="#ffffff" fill-opacity="0.7"/>
      <circle cx="130" cy="30" r="4" fill="#ffffff" fill-opacity="0.6"/>
    </svg>
  </div>

  <!-- Hero -->
  <header class="relative">
    <div class="grain absolute inset-0"></div>
    <div class="max-w-6xl mx-auto px-6 pt-16 pb-24 md:pt-24 md:pb-32">
      <div class="flex flex-col-reverse md:flex-row items-center gap-10">
        <div class="w-full md:w-1/2 reveal">
          <span class="inline-block bg-white/20 text-white/90 px-3 py-1 rounded-full text-xs tracking-widest uppercase">You're Invited</span>
          <h1 class="font-script text-white text-6xl md:text-7xl mt-4 drop-shadow-sm">Ava & Noah</h1>
          <p class="text-white/90 font-display text-2xl mt-2">are tying the knot</p>

          <div class="mt-6 flex items-center gap-4 text-white/90">
            <div class="bg-white/15 backdrop-blur rounded-xl px-4 py-3 shadow-soft">
              <div id="dateText" class="font-display text-lg">Saturday, September 21, 2025</div>
              <div class="text-sm opacity-90">Ceremony at 4:00 PM</div>
            </div>
            <div class="bg-white/15 backdrop-blur rounded-xl px-4 py-3 shadow-soft">
              <div class="font-display text-lg">Willow Garden Estate</div>
              <div class="text-sm opacity-90">Bloomfield, CA</div>
            </div>
          </div>

          <div class="mt-8 flex flex-wrap gap-3">
            <a href="#rsvp" class="inline-flex items-center gap-2 bg-white text-forest-700 hover:bg-forest-50 transition rounded-full px-5 py-3 font-semibold shadow-soft">
              RSVP Now
              <span aria-hidden="true">💌</span>
            </a>
            <a href="#details" class="inline-flex items-center gap-2 bg-white/20 hover:bg-white/25 text-white transition rounded-full px-5 py-3 font-semibold">
              Event Details
              <span aria-hidden="true">📍</span>
            </a>
          </div>

          <!-- Countdown -->
          <div class="mt-8 bg-white/15 backdrop-blur rounded-2xl p-5 inline-flex items-center gap-6 text-white shadow-soft" role="group" aria-label="Countdown to the wedding">
            <div class="text-center">
              <div id="days" class="text-3xl font-display">00</div>
              <div class="text-xs uppercase tracking-wide opacity-90">Days</div>
            </div>
            <div class="text-2xl">:</div>
            <div class="text-center">
              <div id="hours" class="text-3xl font-display">00</div>
              <div class="text-xs uppercase tracking-wide opacity-90">Hours</div>
            </div>
            <div class="text-2xl">:</div>
            <div class="text-center">
              <div id="minutes" class="text-3xl font-display">00</div>
              <div class="text-xs uppercase tracking-wide opacity-90">Minutes</div>
            </div>
            <div class="text-2xl">:</div>
            <div class="text-center">
              <div id="seconds" class="text-3xl font-display">00</div>
              <div class="text-xs uppercase tracking-wide opacity-90">Seconds</div>
            </div>
          </div>
        </div>

        <!-- Hero card -->
        <div class="w-full md:w-1/2 relative reveal">
          <div class="relative bg-white/80 backdrop-blur-xl border border-white/60 rounded-3xl p-6 sm:p-8 shadow-soft overflow-hidden">
            <!-- Floating petals -->
            <div class="absolute -top-4 -left-2 text-blossom-400/70 petal" style="animation-delay:0s;">❀</div>
            <div class="absolute top-10 -right-3 text-blossom-300/80 petal" style="animation-delay:.6s;">❀</div>
            <div class="absolute bottom-6 right-6 text-blossom-500/60 petal" style="animation-delay:1.2s;">❀</div>

            <div class="text-center">
              <div class="font-script text-5xl text-forest-700">Save the Date</div>
              <div class="mt-2 text-sm tracking-widest uppercase text-forest-700/80">A Celebration of Love</div>

              <div class="mt-6 grid grid-cols-3 gap-4">
                <div class="bg-forest-50 rounded-xl p-4">
                  <div class="text-forest-700 text-sm">Ceremony</div>
                  <div class="font-display text-xl">4:00 PM</div>
                </div>
                <div class="bg-forest-50 rounded-xl p-4">
                  <div class="text-forest-700 text-sm">Cocktail</div>
                  <div class="font-display text-xl">5:30 PM</div>
                </div>
                <div class="bg-forest-50 rounded-xl p-4">
                  <div class="text-forest-700 text-sm">Reception</div>
                  <div class="font-display text-xl">7:00 PM</div>
                </div>
              </div>

              <div class="mt-6 text-forest-700/80">
                Willow Garden Estate, 123 Blossom Lane, Bloomfield, CA
              </div>
              <button id="addToCalendar" class="mt-6 inline-flex items-center gap-2 bg-forest-600 hover:bg-forest-700 text-white rounded-full px-5 py-3 font-semibold shadow-soft transition">
                Add to Calendar <span>🗓️</span>
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>

  <!-- Details -->
  <section id="details" class="relative z-10">
    <div class="max-w-6xl mx-auto px-6 py-16 md:py-24">
      <div class="grid md:grid-cols-3 gap-8">
        <div class="reveal bg-white/85 backdrop-blur border border-white/60 rounded-2xl p-6 shadow-soft">
          <div class="flex items-center justify-between">
            <h3 class="font-display text-2xl text-forest-800">The Story</h3>
            <span aria-hidden="true">💞</span>
          </div>
          <p class="mt-3 text-forest-800/80 leading-relaxed">
            From coffee shop strangers to forever partners. We can’t wait to celebrate this next chapter with you.
          </p>
        </div>
        <div class="reveal bg-white/85 backdrop-blur border border-white/60 rounded-2xl p-6 shadow-soft">
          <div class="flex items-center justify-between">
            <h3 class="font-display text-2xl text-forest-800">Dress Code</h3>
            <span aria-hidden="true">🎩</span>
          </div>
          <p class="mt-3 text-forest-800/80 leading-relaxed">
            Garden formal: light suits, floral dresses, and comfortable shoes for the lawn.
          </p>
        </div>
        <div class="reveal bg-white/85 backdrop-blur border border-white/60 rounded-2xl p-6 shadow-soft">
          <div class="flex items-center justify-between">
            <h3 class="font-display text-2xl text-forest-800">Gifts</h3>
            <span aria-hidden="true">🎁</span>
          </div>
          <p class="mt-3 text-forest-800/80 leading-relaxed">
            Your presence is the greatest gift. If you wish, contributions to our honeymoon fund are appreciated.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- RSVP -->
  <section id="rsvp" class="relative z-10">
    <div class="max-w-4xl mx-auto px-6 pb-20">
      <div class="reveal bg-white/90 backdrop-blur border border-white/60 rounded-3xl p-8 shadow-soft">
        <div class="flex items-start gap-6 flex-col md:flex-row">
          <div class="md:w-1/3 w-full">
            <h2 class="font-display text-3xl text-forest-800">RSVP</h2>
            <p class="mt-2 text-forest-800/80">Kindly respond by August 21, 2025.</p>
            <div class="mt-6 bg-forest-50 rounded-xl p-4">
              <div class="text-forest-700 text-sm">Contact</div>
              <div class="font-display text-lg">avaandnoah@wedding.example</div>
            </div>
          </div>

          <div class="md:w-2/3 w-full">
            <!-- Demo note per platform limits -->
            <div class="mb-4 text-forest-800/80 text-sm bg-blossom-100 border border-blossom-200 rounded-lg p-3">
              This is a sample RSVP. It saves locally so you can try it. To collect real responses, publish and connect your own form tool.
            </div>

            <form id="rsvpForm" class="grid sm:grid-cols-2 gap-4">
              <div class="sm:col-span-2">
                <label class="block text-forest-800/90 mb-1">Full Name</label>
                <input required type="text" name="name" class="w-full bg-white border border-forest-100 focus:border-forest-400 focus:ring-2 focus:ring-forest-200 rounded-xl px-4 py-3 outline-none transition" placeholder="Your name"/>
              </div>

              <div>
                <label class="block text-forest-800/90 mb-1">Email</label>
                <input required type="email" name="email" class="w-full bg-white border border-forest-100 focus:border-forest-400 focus:ring-2 focus:ring-forest-200 rounded-xl px-4 py-3 outline-none transition" placeholder="you@example.com"/>
              </div>

              <div>
                <label class="block text-forest-800/90 mb-1">Attendance</label>
                <select name="attendance" class="w-full bg-white border border-forest-100 focus:border-forest-400 focus:ring-2 focus:ring-forest-200 rounded-xl px-4 py-3 outline-none transition">
                  <option value="Accepts with pleasure">Accepts with pleasure</option>
                  <option value="Regretfully declines">Regretfully declines</option>
                </select>
              </div>

              <div>
                <label class="block text-forest-800/90 mb-1">Guests (incl. you)</label>
                <input type="number" name="guests" min="1" max="8" value="1" class="w-full bg-white border border-forest-100 focus:border-forest-400 focus:ring-2 focus:ring-forest-200 rounded-xl px-4 py-3 outline-none transition"/>
              </div>

              <div>
                <label class="block text-forest-800/90 mb-1">Meal Preference</label>
                <select name="meal" class="w-full bg-white border border-forest-100 focus:border-forest-400 focus:ring-2 focus:ring-forest-200 rounded-xl px-4 py-3 outline-none transition">
                  <option>Chef’s Choice</option>
                  <option>Vegetarian</option>
                  <option>Vegan</option>
                  <option>Gluten-Free</option>
                </select>
              </div>

              <div class="sm:col-span-2">
                <label class="block text-forest-800/90 mb-1">Notes (allergies, song requests)</label>
                <textarea name="notes" rows="3" class="w-full bg-white border border-forest-100 focus:border-forest-400 focus:ring-2 focus:ring-forest-200 rounded-xl px-4 py-3 outline-none transition" placeholder="Anything we should know?"></textarea>
              </div>

              <div class="sm:col-span-2 flex items-center gap-3">
                <button type="submit" class="bg-forest-600 hover:bg-forest-700 text-white rounded-full px-6 py-3 font-semibold shadow-soft transition">
                  Send RSVP
                </button>
                <button type="button" id="exportBtn" class="bg-white hover:bg-forest-50 text-forest-700 rounded-full px-6 py-3 font-semibold border border-forest-100 transition">
                  Export Responses (CSV)
                </button>
              </div>
            </form>

            <div id="rsvpSuccess" class="hidden mt-4 bg-forest-50 border border-forest-100 text-forest-800 rounded-xl p-4">
              Thanks! Your RSVP was saved on this device. You can export responses anytime.
            </div>

            <!-- Saved responses (local preview) -->
            <div class="mt-8">
              <div class="flex items-center justify-between">
                <h3 class="font-display text-xl text-forest-800">Your Saved RSVP</h3>
                <button id="clearBtn" class="text-sm text-blossom-700 hover:underline">Clear</button>
              </div>
              <div id="savedList" class="mt-3 text-forest-800/90 bg-white border border-forest-100 rounded-xl p-4">
                No RSVP yet.
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Travel & Stay -->
  <section class="relative z-10">
    <div class="max-w-6xl mx-auto px-6 pb-24">
      <div class="grid md:grid-cols-2 gap-8">
        <div class="reveal bg-white/90 backdrop-blur border border-white/60 rounded-2xl p-6 shadow-soft">
          <div class="flex items-center justify-between">
            <h3 class="font-display text-2xl text-forest-800">Travel</h3>
            <span aria-hidden="true">✈️</span>
          </div>
          <ul class="mt-3 text-forest-800/80 space-y-2">
            <li>Nearest airport: Bloomfield (BMF), 25 min drive.</li>
            <li>Rideshare and onsite parking available.</li>
            <li>Shuttle from Downtown Hotels at 3:15 PM.</li>
          </ul>
        </div>
        <div class="reveal bg-white/90 backdrop-blur border border-white/60 rounded-2xl p-6 shadow-soft">
          <div class="flex items-center justify-between">
            <h3 class="font-display text-2xl text-forest-800">Stay</h3>
            <span aria-hidden="true">🏨</span>
          </div>
          <ul class="mt-3 text-forest-800/80 space-y-2">
            <li>Garden Inn — group rate “AVA&NOAH”.</li>
            <li>Blossom Boutique — walking distance.</li>
            <li>Cozy Airbnbs nearby.</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="relative z-10">
    <div class="max-w-6xl mx-auto px-6 pb-16">
      <div class="bg-white/80 backdrop-blur border border-white/60 rounded-2xl p-6 md:p-8 shadow-soft text-center">
        <div class="font-script text-4xl text-forest-700">With love, Ava & Noah</div>
        <p class="mt-2 text-forest-800/80">We can’t wait to celebrate with you.</p>
        <div class="mt-4 flex items-center justify-center gap-3">
          <a href="#details" class="text-forest-700 hover:underline">Details</a>
          <span class="text-forest-800/40">•</span>
          <a href="#rsvp" class="text-forest-700 hover:underline">RSVP</a>
          <span class="text-forest-800/40">•</span>
          <button id="shareBtn" class="text-forest-700 hover:underline">Share</button>
        </div>
      </div>
    </div>
  </footer>

  <script>
    // Smooth reveal on scroll
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.classList.add('show');
          observer.unobserve(e.target);
        }
      });
    }, { threshold: 0.1 });
    document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

    // Countdown (set your date/time here)
    const weddingDate = new Date('2025-09-21T16:00:00'); // local time
    document.getElementById('dateText').textContent = weddingDate.toLocaleDateString([], { weekday:'long', year:'numeric', month:'long', day:'numeric' });

    function updateCountdown() {
      const now = new Date();
      const diff = weddingDate - now;
      const d = Math.max(0, Math.floor(diff / (1000*60*60*24)));
      const h = Math.max(0, Math.floor((diff / (1000*60*60)) % 24));
      const m = Math.max(0, Math.floor((diff / (1000*60)) % 60));
      const s = Math.max(0, Math.floor((diff / 1000) % 60));
      const pad = (n)=> String(n).padStart(2,'0');
      document.getElementById('days').textContent = pad(d);
      document.getElementById('hours').textContent = pad(h);
      document.getElementById('minutes').textContent = pad(m);
      document.getElementById('seconds').textContent = pad(s);
    }
    updateCountdown();
    setInterval(updateCountdown, 1000);

    // Add to Calendar (.ics download)
    document.getElementById('addToCalendar').addEventListener('click', () => {
      const start = new Date(weddingDate);
      const end = new Date(start.getTime() + 4*60*60*1000); // 4-hour window
      const pad = (n)=> String(n).padStart(2,'0');
      const toICSDate = (d) => `${d.getUTCFullYear()}${pad(d.getUTCMonth()+1)}${pad(d.getUTCDate())}T${pad(d.getUTCHours())}${pad(d.getUTCMinutes())}${pad(d.getUTCSeconds())}Z`;
      const ics =
`BEGIN:VCALENDAR
VERSION:2.0
PRODID:-//Ava & Noah Wedding//EN
BEGIN:VEVENT
UID:${Date.now()}@ava-noah.wedding
DTSTAMP:${toICSDate(new Date())}
DTSTART:${toICSDate(start)}
DTEND:${toICSDate(end)}
SUMMARY:Ava & Noah — Wedding
LOCATION:Willow Garden Estate, 123 Blossom Lane, Bloomfield, CA
DESCRIPTION:Join us for our wedding day! Ceremony at 4:00 PM. Cocktail hour to follow.
END:VEVENT
END:VCALENDAR`;
      const blob = new Blob([ics], {type:'text/calendar'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'Ava-Noah-Wedding.ics';
      document.body.appendChild(a);
      a.click();
      URL.revokeObjectURL(url);
      a.remove();
    });

    // RSVP local save (demo)
    const form = document.getElementById('rsvpForm');
    const success = document.getElementById('rsvpSuccess');
    const list = document.getElementById('savedList');
    const STORAGE_KEY = 'wedding_rsvp_v1';

    function loadRSVP() {
      const raw = localStorage.getItem(STORAGE_KEY);
      if (!raw) { list.textContent = 'No RSVP yet.'; return; }
      try {
        const r = JSON.parse(raw);
        list.innerHTML = `
          <div class="grid sm:grid-cols-2 gap-3">
            <div><span class="font-semibold">Name:</span> ${r.name}</div>
            <div><span class="font-semibold">Email:</span> ${r.email}</div>
            <div><span class="font-semibold">Attendance:</span> ${r.attendance}</div>
            <div><span class="font-semibold">Guests:</span> ${r.guests}</div>
            <div class="sm:col-span-2"><span class="font-semibold">Meal:</span> ${r.meal}</div>
            <div class="sm:col-span-2"><span class="font-semibold">Notes:</span> ${r.notes || '-'}</div>
            <div class="sm:col-span-2 text-xs text-forest-800/70">Saved: ${new Date(r.savedAt).toLocaleString()}</div>
          </div>
        `;
      } catch {
        list.textContent = 'No RSVP yet.';
      }
    }
    loadRSVP();

    form.addEventListener('submit', (e) => {
      e.preventDefault();
      const data = Object.fromEntries(new FormData(form).entries());
      const record = {
        name: data.name?.trim() || '',
        email: data.email?.trim() || '',
        attendance: data.attendance || 'Accepts with pleasure',
        guests: Number(data.guests || 1),
        meal: data.meal || 'Chef’s Choice',
        notes: data.notes?.trim() || '',
        savedAt: new Date().toISOString()
      };
      localStorage.setItem(STORAGE_KEY, JSON.stringify(record));
      success.classList.remove('hidden');
      setTimeout(()=>success.classList.add('hidden'), 3500);
      loadRSVP();
      form.scrollIntoView({ behavior: 'smooth', block: 'center' });
    });

    document.getElementById('clearBtn').addEventListener('click', () => {
      localStorage.removeItem(STORAGE_KEY);
      loadRSVP();
    });

    // Export CSV of the single saved RSVP (demo)
    document.getElementById('exportBtn').addEventListener('click', () => {
      const raw = localStorage.getItem(STORAGE_KEY);
      if (!raw) { alert('No RSVP to export yet.'); return; }
      const r = JSON.parse(raw);
      const headers = ['Name','Email','Attendance','Guests','Meal','Notes','Saved At'];
      const row = [r.name, r.email, r.attendance, r.guests, `"${(r.notes||'').replace(/"/g,'""')}"`, r.savedAt];
      const csv = headers.join(',') + '\n' + row.join(',');
      const blob = new Blob([csv], {type:'text/csv'});
      const url = URL.createObjectURL(blob);
      const a = document.createElement('a');
      a.href = url;
      a.download = 'RSVP.csv';
      document.body.appendChild(a);
      a.click();
      URL.revokeObjectURL(url);
      a.remove();
    });

    // Web Share (if supported)
    document.getElementById('shareBtn').addEventListener('click', async () => {
      const shareData = {
        title: 'Ava & Noah — Wedding',
        text: 'Join us on our special day! RSVP inside.',
        url: location.href
      };
      try {
        if (navigator.share) {
          await navigator.share(shareData);
        } else {
          await navigator.clipboard.writeText(location.href);
          alert('Link copied! Share it with your guests.');
        }
      } catch {}
    });
  </script>
<script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'98097828610b9a6e',t:'MTc1ODEyMTE4Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
