# Application architecture

The Ceres application consists of 3 simple layers:
* **presentation layer** — a client web application
* **logic & data layer** — a RESTful API
* **data storage/external service layer** — 3rd party APIs (MongoDB Atlas, Auth0, etc.)

![A diagram illustrating the three layers outlined above](./app_architecture/ceres_basic_architecture.svg)