Performance Testing with Apache JMeter

This project demonstrates performance testing on the Restful Booker API
 using Apache JMeter.
It includes load testing, stress testing, and report generation.
What I Have Done

Created a JMeter test plan (booking.jmx) to test the following flow:

Login → POST /auth

Create Booking → POST /booking

Search Booking → GET /booking/{booking_id}

Configured a Header Manager with Accept: */*.

Used Gaussian Random Timer with:

Constant Delay: 500ms

Deviation: 2000ms

Designed and executed the following tests:

Load Test:

Step 1: 5 minutes load

Step 2: 10 minutes load

Step 3: 20 minutes load

Stress Test:

Gradually increased users until server bottleneck was identified.

Generated Excel reports (booking-api-test-report.xlsx) with two sheets:

Load Test Report

Stress Test Report

Generated HTML reports for both tests and included screenshots in this README.

⚙️ Prerequisites

Make sure you have the following installed:

Apache JMeter 5.6+

Java JDK 8 or higher

Git

▶️ How to Run the Tests

Clone the Repository

git clone https://github.com/Tama10-10/Performance-testing-using-Jmeter.git


Open the Test Plan in JMeter

Open booking.jmx in JMeter GUI.

Run the Test (Command Line Mode)
Example (for load test):

jmeter -n -t booking.jmx -l booking.jtl -e -o Reports


-n: non-GUI mode

-t: test plan file

-l: log file (booking.jtl)

-e: generate report

-o: output folder (Reports)

Generate HTML Report
After test execution, open the generated Reports/index.html in a browser.

Excel Report
Open booking-api-test-report.xlsx to view Load Test and Stress Test results.

📊 Screenshots
🔹 Load Test Report
<img width="56" height="107" alt="Screenshot 2025-09-06 222508" src="https://github.com/user-attachments/assets/53d8cbd4-2c06-4f88-98b2-0e0b045f48ab" />

🔹 Stress Test Report

🔹 JMeter Statistics
