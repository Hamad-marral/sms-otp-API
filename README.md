
# sms-otp-API

A Node.js Express API for SMS-based OTP verification. This API facilitates secure user authentication through the generation and validation of One-Time Passwords (OTPs) sent via SMS.

## Features
- **OTP Generation**: Creates a unique OTP for each user session.
- **SMS Delivery**: Sends OTPs directly to users' mobile phones via SMS.
- **OTP Validation**: Verifies the entered OTP against the generated one.
- **Timeout Handling**: Configurable expiration times for OTPs to ensure security.
- **Error Handling**: Comprehensive error responses for better API integration and debugging.

## Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/)
- An SMS gateway service (e.g., Twilio, Nexmo)

### Installation
1. **Clone the repository**
   ```bash
   git clone https://github.com/Hamad-marral/sms-otp-API.git
   ```
2. **Navigate to the project directory**
   ```bash
   cd sms-otp-API
   ```
3. **Install dependencies**
   ```bash
   npm install
   ```
4. **Set up environment variables**
   - Create a `.env` file in the root directory.
   - Add your SMS gateway API key and other necessary environment variables.
   ```
   SMS_GATEWAY_API_KEY=your_api_key
   OTP_EXPIRATION_TIME=600000 # time in milliseconds
   ```

### Running the API
To start the server, use the following command:
```bash
npm start
```

## API Endpoints

### Generate OTP
- **Endpoint**: `POST /generate-otp`
- **Description**: Generates and sends an OTP to the specified phone number.
- **Request Body**:
  ```json
  {
    "phoneNumber": "user_phone_number"
  }
  ```

### Verify OTP
- **Endpoint**: `POST /verify-otp`
- **Description**: Verifies the OTP provided by the user.
- **Request Body**:
  ```json
  {
    "phoneNumber": "user_phone_number",
    "otp": "received_otp"
  }
  ```

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
