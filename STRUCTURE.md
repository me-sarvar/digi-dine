## Folder structure of App

```graphql
digidine/
│
├── frontend/              # Flutter Web project (guest app, admin, kitchen)
│
├── backend/               # FastAPI backend project
│
├── infrastructure/        # Deployment, Docker, CI/CD files
│
└── docs/                  # Documentation (flowcharts, diagrams, tech docs)
```
## Folder structure of Backend

```graphql
backend/
├── app/
│   ├── main.py                  # FastAPI app entry point
│   ├── api/                     # API route groupings
│   │   ├── v1/                  # Versioned API for long-term stability
│   │   │   ├── routes_guest.py
│   │   │   ├── routes_admin.py
│   │   │   ├── routes_kitchen.py
│   │   │   ├── routes_auth.py
│   │   │   ├── routes_restaurant.py
│   │   │   └── __init__.py
│   │   └── __init__.py
│   │
│   ├── core/                    # Core configurations
│   │   ├── config.py
│   │   ├── security.py          # JWT, password hashing, token logic
│   │   └── utils.py
│   │
│   ├── db/                      # Database models & session setup
│   │   ├── session.py
│   │   ├── base.py              # Base model
│   │   ├── models/              # SQLAlchemy models
│   │   │   ├── user.py
│   │   │   ├── restaurant.py
│   │   │   ├── table.py
│   │   │   ├── menu.py
│   │   │   ├── order.py
│   │   │   ├── utensil.py
│   │   │   └── session_token.py
│   │   └── schemas/             # Pydantic request/response models
│   │       ├── user.py
│   │       ├── restaurant.py
│   │       ├── table.py
│   │       ├── menu.py
│   │       ├── order.py
│   │       └── utensil.py
│   │
│   ├── services/                # Business logic, QR generation, PIN rotation
│   │   ├── auth_service.py
│   │   ├── order_service.py
│   │   ├── restaurant_service.py
│   │   ├── qr_service.py
│   │   ├── websocket_manager.py
│   │   └── session_token_service.py
│   │
│   ├── websocket/               # WebSocket event handlers
│   │   ├── guest_ws.py
│   │   ├── kitchen_ws.py
│   │   ├── admin_ws.py
│   │   └── __init__.py
│   │
│   └── middleware/              # Custom middlewares (CORS, auth guards)
│       └── auth_middleware.py
│
├── tests/                       # Unit & integration tests
│   ├── api/
│   ├── services/
│   ├── db/
│   └── conftest.py
│
├── alembic/                     # Database migrations
│
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
└── README.md
```

## Folder structure of Frontend

```graphql
frontend/
├── guest_app/                 # Guest ordering system (multi-tenant ready)
│   └── lib/
│       ├── main.dart
│       ├── screens/
│       ├── widgets/
│       ├── models/
│       ├── services/
│       └── theme/
│
├── admin_dashboard/           # Global management dashboard
│   └── lib/
│       ├── main.dart
│       ├── screens/
│       ├── widgets/
│       ├── models/
│       ├── services/
│       └── theme/
│
├── kitchen_dashboard/         # Kitchen order management
│   └── lib/
│       ├── main.dart
│       ├── screens/
│       ├── widgets/
│       ├── models/
│       ├── services/
│       └── theme/
│
└── shared_packages/           # Optional shared Dart packages
    ├── models/
    ├── api_client/
    └── utilities/

```

## Folder structure of Infrastructure

```graphql
infrastructure/
├── docker-compose.yml
├── nginx/                     # Reverse proxy configs
├── certs/                     # SSL certificates if needed
└── ci-cd/                     # GitHub Actions, pipelines, etc.
```