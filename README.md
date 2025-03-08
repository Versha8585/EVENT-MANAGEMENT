# EVENT-MANAGEMENT
<html>
<head></head>
<body>
    <header>
        <h1>Welcome to VR TechCon 2025</h1>
        <p>The Ultimate Technology and Programming Conference</p>
    </header>
    <nav>
        <a href="#about">About</a> |
        <a href="#schedule">Schedule</a> |
        <a href="#speakers">Speakers</a> |
        <a href="#contact">Contact</a>
    </nav>
    <section id="about">
        <h2>About the Event</h2>
        <p>GeeksforGeeks TechCon 2025 brings together leading minds in programming,
          tech, and innovation. Join us for a day of insightful talks, hands-on workshops,
          and an opportunity to network with fellow geeks and professionals from all around the world.</p>
    </section>
    <section id="schedule">
        <h2>Event Schedule</h2>
        <table>
            <thead>
                <tr>
                    <th>Time</th>
                    <th>Session</th>
                    <th>Contest</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>9:00 AM</td>
                    <td>Opening Keynote</td>
                    <td>GeeksforGeeks Coding Plateform</td>
                </tr>
                <tr>
                    <td>10:30 AM</td>
                    <td>Understanding AI and Machine Learning</td>
                    <td>Mr. Arvind Kumar</td>
                </tr>
                <tr>
                    <td>1:00 PM</td>
                    <td>Lunch Break</td>
                    <td>-</td>
                </tr>
                <tr>
                    <td>2:00 PM</td>
                    <td>Exploring the Future of Cloud Computing</td>
                    <td>Ms. Neha Gupta</td>
                </tr>
            </tbody>
        </table>
    </section>
    <section id="speakers">
        <h2>Meet the Speakers</h2>
        <ul>
            <li><strong>Dr. Radhika Sharma:</strong> AI Expert and Researcher</li>
            <li><strong>Mr. Arvind Kumar:</strong> Senior Data Scientist at TechWave</li>
            <li><strong>Ms. Neha Gupta:</strong> Cloud Computing Specialist at CloudTech</li>
            <li><strong>Mr. Sandeep Reddy:</strong> Full Stack Developer and Open-Source Contributor</li>
        </ul>
    </section>
    <section id="contact">
        <h2>Contact Us</h2>
        <form>
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name"><br><br>
            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email"><br><br>
            <label for="message">Message:</label><br>
            <textarea id="message" name="message" rows="4"></textarea><br><br>
            <button type="submit">Send</button>
        </form>
    </section>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Event Calendar</title>
    <link href='https://cdn.jsdelivr.net/npm/fullcalendar@5.11.0/main.min.css' rel='stylesheet' />
    <script src='https://cdn.jsdelivr.net/npm/fullcalendar@5.11.0/main.min.js'></script>
</head>
<body>

<div id='calendar'></div>

<script>
    document.addEventListener('DOMContentLoaded', function() {
        var calendarEl = document.getElementById('calendar');
        var calendar = new FullCalendar.Calendar(calendarEl, {
            initialView: 'dayGridMonth',
            events: [
                { title: 'Event 1', start: '2025-03-10' },
                { title: 'Event 2', start: '2025-03-15' }
            ]
        });
        calendar.render();
    });
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Event Management</title>
    <link rel="stylesheet" href="styles.css">
    <script src="script.js" defer></script>
    
    <!-- FullCalendar CSS & JS -->
    <link href="https://cdn.jsdelivr.net/npm/fullcalendar@5.11.0/main.min.css" rel="stylesheet" />
    <script src="https://cdn.jsdelivr.net/npm/fullcalendar@5.11.0/main.min.js"></script>
    
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="#home" onclick="scrollToSection('home')">Home</a></li>
                <li><a href="#events" onclick="scrollToSection('events')">Events</a></li>
                <li><a href="#calendar" onclick="scrollToSection('calendar')">Calendar</a></li>
                <li><a href="#payment" onclick="window.location.href='payment.html'">Payment</a></li>
                <li><a href="#contact" onclick="scrollToSection('contact')">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="home" class="hero">
        <h2>Unforgettable Events Await You!</h2>
        <p>Experience the best event setups with premium services for up to 16 guests, starting at ₹45,000.</p>
        <button class="btn-primary" onclick="scrollToSection('events')">Explore Now</button>
    </section>
    
    <section id="events" class="event-list">
        <h2>Upcoming Events</h2>
        <div class="event">
            <img src="pool-party.jpg" alt="Pool Party">
            <h3>Pool Party</h3>
            <p>Enjoy a luxurious poolside experience with music, drinks, and fun.</p>
        </div>
        <div class="event">
            <img src="fun-party.jpg" alt="Fun Party">
            <h3>Fun Party</h3>
            <p>Experience thrilling games, interactive activities, and non-stop entertainment.</p>
        </div>
    </section>

    <!-- Calendar Section -->
    <section id="calendar">
        <h2>Event Calendar</h2>
        <div id="eventCalendar"></div>
    </section>

    <footer>
        <p>&copy; 2024 Event Management | Designed for a Premium Experience</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
document.addEventListener('DOMContentLoaded', function() {
    var calendarEl = document.getElementById('eventCalendar');
    var calendar = new FullCalendar.Calendar(calendarEl, {
        initialView: 'dayGridMonth',
        events: [
            { title: 'Pool Party', start: '2025-03-15' },
            { title: 'Fun Party', start: '2025-03-20' }
        ]
    });
    calendar.render();
});

function scrollToSection(id) {
    document.getElementById(id).scrollIntoView({
        behavior: 'smooth'
    });
}
#calendar {
    background: #29294d;
    padding: 50px;
    text-align: center;
    color: white;
}
#eventCalendar {
    max-width: 900px;
    margin: auto;
    background: white;
    padding: 15px;
    border-radius: 10px;
}
git add .
git commit -m "Added event calendar"
git push origin main

