# Movie Streaming Service

Welcome to the Movie Streaming Service! This project aims to provide a fully functional movie streaming platform where users can watch and discover movies.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- **User Authentication**: Secure sign-up and login functionalities.
- **Movie Database**: Extensive collection of movies with details like title, genre, and description.
- **Streaming**: Smooth streaming experience with high-quality video playback.
- **Search and Filter**: Easily search and filter movies based on different criteria.
- **Watchlist**: Add movies to your watchlist to view later.
- **Reviews and Ratings**: Leave reviews and ratings for movies you've watched.

## Installation

### Prerequisites

- Node.js
- npm or yarn
- MongoDB
- (Optional) Docker

### Steps

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/movie-streaming-service.git
    cd movie-streaming-service
    ```

2. Install dependencies:
    ```sh
    npm install
    # or
    yarn install
    ```

3. Set up environment variables:
    Create a `.env` file in the root directory and add your MongoDB URI and other necessary environment variables.

    ```
    MONGODB_URI=your_mongodb_uri
    JWT_SECRET=your_jwt_secret
    ```

4. Start the development server:
    ```sh
    npm start
    # or
    yarn start
    ```

5. (Optional) Using Docker:
    ```sh
    docker-compose up --build
    ```

## Usage

1. Open your web browser and navigate to `http://localhost:3000`.
2. Sign up for a new account or log in if you already have one.
3. Browse through the movie collection and start streaming!

## Technologies Used

- **Frontend**: React, Redux, CSS
- **Backend**: Node.js, Express
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Video Streaming**: HTML5 Video, HLS.js

## Contributing

Contributions are welcome! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For any questions or feedback, please reach out to me at [sidcalitiger@gmail.com](mailto:sidcalitiger@gmail.com).

---

Happy streaming!
