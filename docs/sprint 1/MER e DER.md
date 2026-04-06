---
id: d0e9e8de-feeb-4da5-8cae-83c276d297b5
---
# MER e DER — Banco de Dados Trivio

## MER — Modelo Entidade-Relacionamento

```mermaid
erDiagram
    CLIENT {
        bigint client_id PK
        string name
        string cpf
        string cnpj
        string email
        string phone
        boolean active
    }

    EMPLOYEE {
        bigint employee_id PK
        string name
        string email
        string password
        boolean is_admin
        boolean active
    }

    EQUIPMENT {
        bigint equipment_id PK
        string name
        string model
        string manufacturer
        boolean active
    }

    REQUIREMENT {
        bigint requirement_id PK
        string name
        string description
        boolean active
    }

    CONTRACT {
        bigint contract_id PK
        bigint client_id FK
        date initial_date
        date final_date
        bigint recurrence_maintenance
        boolean active
    }

    MAINTENANCE {
        bigint maintenance_id PK
        bigint contract_id FK
        date maintenance_date
        boolean preventive
        string type
        string status
    }

    CLIENT ||--o{ CONTRACT : "possui"
    CONTRACT }o--o{ EQUIPMENT : "inclui"
    CONTRACT }o--o{ REQUIREMENT : "exige"
    CONTRACT ||--o{ MAINTENANCE : "gera"
    MAINTENANCE }o--o{ EMPLOYEE : "executada por"
```

### Entidades e Atributos

#### client
| Atributo | Tipo | Restrições |
|---|---|---|
| **client_id** (PK) | BIGINT | NOT NULL, AUTO |
| name | VARCHAR(100) | NOT NULL |
| cpf | VARCHAR(15) | |
| cnpj | VARCHAR(19) | |
| email | VARCHAR(100) | |
| phone | VARCHAR(20) | |
| active | BOOLEAN | |

#### employee
| Atributo | Tipo | Restrições |
|---|---|---|
| **employee_id** (PK) | BIGINT | NOT NULL, AUTO |
| name | VARCHAR(100) | NOT NULL |
| email | VARCHAR(100) | NOT NULL |
| password | VARCHAR(100) | NOT NULL |
| is_admin | BOOLEAN | |
| active | BOOLEAN | |

#### equipment
| Atributo | Tipo | Restrições |
|---|---|---|
| **equipment_id** (PK) | BIGINT | NOT NULL, AUTO |
| name | VARCHAR(100) | NOT NULL |
| model | VARCHAR(50) | |
| manufacturer | VARCHAR(50) | |
| active | BOOLEAN | |

#### requirement
| Atributo | Tipo | Restrições |
|---|---|---|
| **requirement_id** (PK) | BIGINT | NOT NULL, AUTO |
| name | VARCHAR(100) | NOT NULL |
| description | VARCHAR(255) | |
| active | BOOLEAN | DEFAULT TRUE |

#### contract
| Atributo | Tipo | Restrições |
|---|---|---|
| **contract_id** (PK) | BIGINT | NOT NULL, AUTO |
| client_id (FK) | BIGINT | NOT NULL |
| initial_date | DATE | NOT NULL |
| final_date | DATE | NOT NULL |
| recurrence_maintenance | BIGINT | NOT NULL |
| active | BOOLEAN | DEFAULT TRUE |

#### maintenance
| Atributo | Tipo | Restrições |
|---|---|---|
| **maintenance_id** (PK) | BIGINT | NOT NULL, AUTO |
| contract_id (FK) | BIGINT | NOT NULL |
| maintenance_date | DATE | NOT NULL |
| preventive | BOOLEAN | NOT NULL |
| type | ENUM | NOT NULL (`PREVENTIVA`, `CORRETIVA`, `MELHORIA`) |
| status | ENUM | NOT NULL (`SCHEDULED`, `STARTED`, `COMPLETED`) |

#### contract_equipment _(tabela associativa)_
| Atributo | Tipo | Restrições |
|---|---|---|
| **id** (PK) | BIGINT | NOT NULL, AUTO |
| contract_id (FK) | BIGINT | NOT NULL |
| equipment_id (FK) | BIGINT | NOT NULL |
| active | BOOLEAN | DEFAULT TRUE |

#### contract_requirement _(tabela associativa)_
| Atributo | Tipo | Restrições |
|---|---|---|
| **id** (PK) | BIGINT | NOT NULL, AUTO |
| contract_id (FK) | BIGINT | NOT NULL |
| requirement_id (FK) | BIGINT | NOT NULL |
| active | BOOLEAN | DEFAULT TRUE |

#### maintenance_employee _(tabela associativa)_
| Atributo | Tipo | Restrições |
|---|---|---|
| **id** (PK) | BIGINT | NOT NULL, AUTO |
| maintenance_id (FK) | BIGINT | NOT NULL |
| employee_id (FK) | BIGINT | NOT NULL |
| active | BOOLEAN | DEFAULT TRUE |

---

### Relacionamentos

| Entidade A | Cardinalidade | Entidade B | Descrição |
|---|---|---|---|
| client | 1 : N | contract | Um cliente pode ter muitos contratos |
| contract | N : M | equipment | Um contrato inclui vários equipamentos; um equipamento pode estar em vários contratos (`contract_equipment`) |
| contract | N : M | requirement | Um contrato possui vários requisitos; um requisito pode estar em vários contratos (`contract_requirement`) |
| contract | 1 : N | maintenance | Um contrato pode ter várias manutenções |
| maintenance | N : M | employee | Uma manutenção envolve vários funcionários; um funcionário pode atuar em várias manutenções (`maintenance_employee`) |

---

## DER — Diagrama Entidade-Relacionamento

```mermaid
erDiagram
    client {
        bigint client_id PK
        varchar name
        varchar cpf
        varchar cnpj
        varchar email
        varchar phone
        boolean active
    }

    employee {
        bigint employee_id PK
        varchar name
        varchar email
        varchar password
        boolean is_admin
        boolean active
    }

    equipment {
        bigint equipment_id PK
        varchar name
        varchar model
        varchar manufacturer
        boolean active
    }

    requirement {
        bigint requirement_id PK
        varchar name
        varchar description
        boolean active
    }

    contract {
        bigint contract_id PK
        bigint client_id FK
        date initial_date
        date final_date
        bigint recurrence_maintenance
        boolean active
    }

    maintenance {
        bigint maintenance_id PK
        bigint contract_id FK
        date maintenance_date
        boolean preventive
        varchar type
        varchar status
    }

    contract_equipment {
        bigint id PK
        bigint contract_id FK
        bigint equipment_id FK
        boolean active
    }

    contract_requirement {
        bigint id PK
        bigint contract_id FK
        bigint requirement_id FK
        boolean active
    }

    maintenance_employee {
        bigint id PK
        bigint maintenance_id FK
        bigint employee_id FK
        boolean active
    }

    client ||--o{ contract : "possui"
    contract ||--o{ contract_equipment : "inclui"
    equipment ||--o{ contract_equipment : "pertence a"
    contract ||--o{ contract_requirement : "exige"
    requirement ||--o{ contract_requirement : "pertence a"
    contract ||--o{ maintenance : "gera"
    maintenance ||--o{ maintenance_employee : "envolve"
    employee ||--o{ maintenance_employee : "executa"
```