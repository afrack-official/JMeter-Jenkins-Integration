# JMeter Integration with Jenkins Pipeline
This project demonstrates the integration of Apache JMeter with Jenkins to automate load testing in a Continuous Integration/Continuous Deployment (CI/CD) pipeline. The goal is to ensure that applications can handle expected loads and perform well under stress, all while streamlining the testing process.

# High-Level Steps
Set Up JMeter: Create a JMeter test plan that simulates user interactions with your application. This plan defines the load scenarios, including the number of virtual users and the endpoints to be tested.

> Configure Jenkins: Install necessary Jenkins plugins (e.g., JMeter Plugin and Performance Plugin) to facilitate JMeter test execution and result reporting.

> Create a Jenkins Pipeline: Develop a Jenkins pipeline that includes a stage to execute the JMeter test plan automatically whenever code is pushed to the repository or on a schedule.

> Execute Load Tests: The pipeline runs the JMeter tests in non-GUI mode, collecting performance metrics and sending the data to InfluxDB. This allows for real-time monitoring and analysis. You can also view live updates on the Grafana dashboard, providing visual insights into application performance during and after the tests.

> Auto Deploy VMs: A script included in the repository automates the deployment of virtual machines according to the load test requirements. This ensures that the testing environment scales dynamically based on the load being tested.
