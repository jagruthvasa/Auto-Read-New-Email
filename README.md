# Email Parser Service

This project is an email parsing service that connects to an IMAP email server, listens for new messages, and processes them. It is built using Spring Boot and Jakarta Mail.

## Features

- Connects to an IMAP email server
- Listens for new incoming messages/mails
- Extracts and prints message details including subject, sender, recipients, CCs, body, and attachment names

## Prerequisites

- Java 22
- Gradle 7.0 or higher
- Access to an IMAP email account (e.g., Gmail)
- Make sure to enable IMAP in your gmail settings
- Make sure to create the app password for your gmail

## Getting Started

Follow these steps to set up and run the project locally:

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/email-parser-service.git
cd email-parser-service
```

### 2. Configure Email Credentials

Make sure to add below properties in this file `src/main/resources/application.properties`

```properties
email.address=your_email_address
email.password=your_app_password(not your email passwoed)
```

### 3. Build the Project

Use Gradle to build the project:

```bash
./gradlew build
```

### 4. Run the Application

Start the application using Gradle:

```bash
./gradlew bootRun
```

### 5. Verify Operation

After starting the application, check the console output to verify that the IMAP connection is established successfully and that new messages are being processed. The application will print details of incoming emails, including subject, sender, recipients, body, and attachments.

## Project Structure

- `src/main/java/com/emailparser/`: Contains the main application code.
  - `EmailService.java`: Handles email connection and retrieval.
  - `MessageHandlerService.java`: Processes and prints email messages.
  - `EmailParserApplication.java`: Main class to run the Spring Boot application.
- `src/main/resources/application.properties`: Configuration file for email credentials and server settings.

