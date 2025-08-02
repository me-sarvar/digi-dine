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
├── src/
│   ├── main.ts                        # NestJS app entry point
│   ├── app.module.ts                 # Root module
│
│   ├── auth/                         # Auth module (JWT, guards, roles)
│   │   ├── auth.module.ts
│   │   ├── auth.controller.ts
│   │   ├── auth.service.ts
│   │   └── jwt.strategy.ts
│
│   ├── user/                         # User management
│   │   ├── user.module.ts
│   │   ├── user.controller.ts
│   │   ├── user.service.ts
│   │   └── user.entity.ts
│
│   ├── restaurant/                   # Restaurant logic
│   │   ├── restaurant.module.ts
│   │   ├── restaurant.controller.ts
│   │   ├── restaurant.service.ts
│   │   └── restaurant.entity.ts
│
│   ├── table/                        # Table sessions & management
│   │   ├── table.module.ts
│   │   ├── table.controller.ts
│   │   ├── table.service.ts
│   │   └── table.entity.ts
│
│   ├── menu/                         # Menu items
│   │   ├── menu.module.ts
│   │   ├── menu.controller.ts
│   │   ├── menu.service.ts
│   │   └── menu.entity.ts
│
│   ├── order/                        # Order handling
│   │   ├── order.module.ts
│   │   ├── order.controller.ts
│   │   ├── order.service.ts
│   │   └── order.entity.ts
│
│   ├── utensil/                      # Utensil tracking
│   │   ├── utensil.module.ts
│   │   ├── utensil.controller.ts
│   │   ├── utensil.service.ts
│   │   └── utensil.entity.ts
│
│   ├── qr/                           # QR & PIN generation
│   │   ├── qr.module.ts
│   │   ├── qr.service.ts
│   │   └── pin-rotation.service.ts
│
│   ├── websocket/                    # Gateway for real-time updates
│   │   ├── events.gateway.ts
│   │   ├── guest.gateway.ts
│   │   ├── kitchen.gateway.ts
│   │   └── admin.gateway.ts
│
│   ├── common/                       # DTOs, interfaces, constants, guards
│   │   ├── decorators/
│   │   ├── guards/
│   │   ├── interceptors/
│   │   └── dtos/
│
├── test/                             # Unit & integration tests
│
├── prisma/                           # If using Prisma instead of TypeORM
│   └── schema.prisma
│
├── ormconfig.ts or .env             # DB config (for TypeORM or Prisma)
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