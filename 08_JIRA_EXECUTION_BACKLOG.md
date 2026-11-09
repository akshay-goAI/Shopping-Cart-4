# 08_JIRA_EXECUTION_BACKLOG.md

## 1. Upstream — Platforms & Tracks

| Platform | In scope? | Source |
|---|---|---|
| Web | Yes | `00_PROJECT_CLASSIFICATION_AND_INTAKE.md` §2b |
| Mobile | No | `00_PROJECT_CLASSIFICATION_AND_INTAKE.md` §2b |
| Backend API (surface) | No | `00_PROJECT_CLASSIFICATION_AND_INTAKE.md` §2b |

| Track | Required? | Why |
|---|---|---|
| Frontend | Yes | Required for user interface development. |
| Mobile | No | Not in scope for this project. |
| Backend | No | Not in scope for this project. |
| Data | No | Not applicable. |
| Infra/DevOps | Yes | Required for deployment and infrastructure management. |
| QA | Yes | Always required for delivered software. |
| Security | No | Not applicable. |
| AI/Automation | No | Not applicable. |

## 2. Epics

| Epic | Goal | Included Stories | Owner |
|---|---|---|---|
| Shopping Cart UI Development | Create a minimal shopping cart UI | User Stories for adding, removing, viewing items, and checkout | Frontend Developer 1 |

## 3. User Stories

| Story | Platforms | Persona | Value statement | Acceptance criteria |
|---|---|---|---|---|
| Add Item to Cart | Web | Shopper | Users can add items to their shopping cart. | Given a product, when the user clicks "Add to Cart", then the item should be added to the cart. |
| Remove Item from Cart | Web | Shopper | Users can remove items from their shopping cart. | Given an item in the cart, when the user clicks "Remove", then the item should be removed from the cart. |
| View Cart | Web | Shopper | Users can view the items in their shopping cart. | Given items in the cart, when the user clicks on the cart icon, then the cart should display the items. |
| Checkout | Web | Shopper | Users can proceed to checkout from the shopping cart. | Given items in the cart, when the user clicks "Checkout", then the user should be directed to the checkout page. |

## 4. Engineering Tasks

### Frontend Tasks

| Task | Story Link | Component | Owner | Dependency |
|---|---|---|---|---|
| Implement Add Item functionality | User Story: Add Item to Cart | frontend | Frontend Developer 1 | N/A |
| Implement Remove Item functionality | User Story: Remove Item from Cart | frontend | Frontend Developer 1 | N/A |
| Implement View Cart functionality | User Story: View Cart | frontend | Frontend Developer 2 | N/A |
| Implement Checkout functionality | User Story: Checkout | frontend | Frontend Developer 2 | N/A |

### DevOps Tasks

| DevOps Task | Story/Epic Link | Environment | Owner | Dependency |
|---|---|---|---|---|
| Set up CI/CD pipeline for deployment | Epic: Shopping Cart UI Development | Production | DevOps Engineer | N/A |

### QA Tasks

| QA Task | Story Link | Test Type | Owner | Evidence |
|---|---|---|---|---|
| Validate Add Item functionality | User Story: Add Item to Cart | Functional | QA Engineer | Test report |
| Validate Remove Item functionality | User Story: Remove Item from Cart | Functional | QA Engineer | Test report |
| Validate View Cart functionality | User Story: View Cart | Functional | QA Engineer | Test report |
| Validate Checkout functionality | User Story: Checkout | Functional | QA Engineer | Test report |

## 5. Traceability Matrix

| Requirement | Epic | Story | Task | Test |
|---|---|---|---|---|
| Users can add items to their shopping cart. | Shopping Cart UI Development | Add Item to Cart | Implement Add Item functionality | Validate Add Item functionality |
| Users can remove items from their shopping cart. | Shopping Cart UI Development | Remove Item from Cart | Implement Remove Item functionality | Validate Remove Item functionality |
| Users can view items in their shopping cart. | Shopping Cart UI Development | View Cart | Implement View Cart functionality | Validate View Cart functionality |
| Users can proceed to checkout. | Shopping Cart UI Development | Checkout | Implement Checkout functionality | Validate Checkout functionality |

## 6. Jira Import JSON

{
  "issues": [
    {
      "summary": "Add Item to Cart",
      "description": "Users can add items to their shopping cart.",
      "acceptanceCriteria": "Given a product, when the user clicks 'Add to Cart', then the item should be added to the cart.",
      "platforms": ["Web"],
      "component": "frontend",
      "labels": ["web", "frontend"],
      "assignee": "Frontend Developer 1",
      "reviewer": "Tech Lead"
    },
    {
      "summary": "Remove Item from Cart",
      "description": "Users can remove items from their shopping cart.",
      "acceptanceCriteria": "Given an item in the cart, when the user clicks 'Remove', then the item should be removed from the cart.",
      "platforms": ["Web"],
      "component": "frontend",
      "labels": ["web", "frontend"],
      "assignee": "Frontend Developer 1",
      "reviewer": "Tech Lead"
    },
    {
      "summary": "View Cart",
      "description": "Users can view the items in their shopping cart.",
      "acceptanceCriteria": "Given items in the cart, when the user clicks on the cart icon, then the cart should display the items.",
      "platforms": ["Web"],
      "component": "frontend",
      "labels": ["web", "frontend"],
      "assignee": "Frontend Developer 2",
      "reviewer": "Tech Lead"
    },
    {
      "summary": "Checkout",
      "description": "Users can proceed to checkout from the shopping cart.",
      "acceptanceCriteria": "Given items in the cart, when the user clicks 'Checkout', then the user should be directed to the checkout page.",
      "platforms": ["Web"],
      "component": "frontend",
      "labels": ["web", "frontend"],
      "assignee": "Frontend Developer 2",
      "reviewer": "Tech Lead"
    },
    {
      "summary": "Set up CI/CD pipeline for deployment",
      "description": "Set up a CI/CD pipeline for the shopping cart UI deployment.",
      "platforms": ["Web"],
      "component": "devops",
      "labels": ["web-deploy"],
      "assignee": "DevOps Engineer",
      "reviewer": "DevOps Lead"
    }
  ]
}

## 7. Validation Checklist

- [ ] Skeleton preserved; Sources + Templates used set
- [ ] Platform coverage + channel devops tasks
- [ ] Traceability matrix filled
- [ ] JSON includes platform labels / assignees
- [ ] Ready for Phase 09 (and P08 validate)

## 8. Phase Exit Criteria checklist
- [ ] All epics and stories defined
- [ ] Engineering tasks outlined and assigned
- [ ] QA tasks specified and assigned
- [ ] DevOps tasks defined and assigned
- [ ] Validation checklist completed