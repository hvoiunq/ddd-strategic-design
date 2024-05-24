# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전

| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
|  |  |  |

## 모델링
### 상품
- `Product` 는 식별자, `ProductName`, `ProductPrice` 을 가진다.

### 메뉴 그룹
- `MenuGroup` 은 식별자, `MenuGroupName` 을 가진다.

### 메뉴
- `Menu` 는 식별자, `MenuName`, `MenuPrice`, `MenuGroup`, `MenuDisplayStatus`, `MenuProducts` 를 가진다.
- `Menu`에서 `MenuProducts`를 생성한다.
- `Menu`에서 `MenuDisplayStatus` 를 변경한다.
- `Menu`에서 `MenuProduct` 가격의 총 `Price`을 계산한다.

### 메뉴 상품
- `MenuProduct` 는 `Product`, `Quantity` 을 가진다.
- `MenuProduct` 에서 `Product` 의 총 `Price` 을 계산한다.

### 주문 테이블
- `OrderTable` 은 식별자, `OrderTableName`, `NumberOfGuests`, `Occupied` 를 가진다.
- `OrderTable` 에서 `Occupied`를 변경한다.

### 배달 주문
- `Order` 는 `OrderType` 중 `DELIVERY_ORDER` 를 가진다.
- `Order` 는 식별자, `OrderStatus`, 주문 일시, `DeliveryAddress`, `OrderLineItems` 을 가진다.
- `Order` 에서 `OrderLineItems` 를 생성한다.
- `OrderLineItems`은 선택한 `Menu`와 `Quantity`과 총 `Price`을 가진다.
- `Order` 에서 `OrderStatus` 를 변경한다.
- `OrderStatus` 는 `Waiting` → `Accepted` → `Served` → `Delivering` → `Delivered` → `Completed` 를 가진다.
  ```mermaid
  ---
  title: Delivery OrderStatus
  ---
  flowchart LR
    A[Waiting] --> D(Accepted)
    D --> E(Served)
    E --> F(Delivering)
    F --> G(Delivered)
    G --> H[Completed]
  ```

### 포장 주문
- `Order` 는 `OrderType` 중 `TAKEOUT` 를 가진다.
- `Order` 는 식별자, `OrderStatus`, 주문 일시, `OrderLineItems` 을 가진다.
- `Order` 에서 `OrderLineItems` 를 생성한다.
- `OrderLineItems`은 선택한 `Menu`와 `Quantity` 과 총 `Price` 을 가진다.
- `Order` 에서 `OrderStatus` 를 변경한다.
- `OrderStatus` 는 `Waiting` → `Accepted` → `Served` → `Completed` 를 가진다.
  ```mermaid
  ---
  title: Takeout OrderStatus
  ---
  flowchart LR
    A[Waiting] --> D(Accepted)
    D --> E(Served)
    E --> H[Completed]
  ```

### 매장 주문
- `Order` 는 `OrderType` 중 `EAT_IN` 를 가진다.
- `Order` 는 식별자, `OrderStatus`, 주문 일시, `OrderLineItems`, `OrderTable`을 가진다.
- `Order` 에서 `OrderLineItems` 를 생성한다.
- `OrderLineItems`은 선택한 `Menu`와 `Quantity` 과 총 `Price` 을 가진다.
- `Order` 에서 `OrderStatus` 를 변경한다.
- `OrderStatus` 는 `Waiting` → `Accepted` → `Served` →  `Completed` 를 가진다.
  ```mermaid
  ---
  title: EatIn OrderStatus
  ---
  flowchart LR
    A[Waiting] --> D(Accepted)
    D --> E(Served)
    E --> H[Completed]
  ```

### 기타
#### 주문 등록 정책
- `배달 주문`: `메뉴`가 `노출된 메뉴`이고 `배달 주소`가 있어야 `메뉴`가 0개 이상이어야 등록이 가능하다.
- `매장 주문`: `메뉴`가 `노출된 메뉴`이고 `주문 테이블`이 있어야 등록이 가능하다.
- `포장 주문`: `메뉴`가 `노출된 메뉴`이고 `메뉴`가 0개 이상이어야 등록이 가능하다.
#### 주문상태 변경 정책
- `주문`의 유형별로 정의된 `주문상태`의 순서대로만 변경이 가능하다.
