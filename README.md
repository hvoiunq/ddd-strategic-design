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
|고객     | client  |  - 키친포스 사용 대상의 총칭으로, 손님/사장님으로 구분할 수 있다.  |
|손님     | customer  |  - 주문을 하는 모든 키친포스 고객을 뜻한다.  |
|사장님    | manager  |  - 키친포스 내 매장의 메뉴를 관리하는 고객을 뜻한다.   |
|매장     | restaurant  |  - 손님이 방문하여 매장 주문을 할 수 있는 장소  |
|상품     | product  |  - 메뉴의 단위 요리를 표현한다. (음식의 재료를 표현하는 것은 아님)  |
|상품 이름  | product name   |  - 사장님인 경우에 등록이 가능하다.  |
|상품 가격  | product price  |  - 상품을 표현하는 이름으로, 등록할 때 필요하다. (단, 비속어 포함 불가)  |
|메뉴 그룹  | menu group  |  - 상품 가격으로, 0원 이상 등록이 되어야 한다.   |
|메뉴     | menu  |  - 가격은 상품 등록 후 변경이 가능하다. (단, 메뉴에 속한 경우 메뉴 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨짐.)  |
|메뉴 노출  | menu display  |  - 메뉴들을 묶어서 표현하는 단위이다.   |
|메뉴 가격  | menu price  |  - 사장님이 등록 후 손님이 주문할 수 있는 단위이며, 한 개 이상 상품으로 구성된다.  |
|주문 테이블 | order table  |  - 손님이 메뉴에 대한 정보를 볼 수 있다는 것을 의미한다.  |
|빈 테이블  | cleared table  |  - 사장님이 등록할 수 있는 메뉴의 가격이다.   |
|주문     | order   |  - 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.  |
|배달 주문  | delivery  |  - 매장에서 관리되는 테이블로 매장 식사 손님용.   |
|포장 주문  | takeout   |  - 매장 식사 손님이 모든 식사를 마치는 경우 테이블을 치운다.  |
|매장 주문  | eat in  |  - 테이블을 치운 상태를 빈 테이블이라고 표현한다.  |
|배달 주소  | delivery address  |  - 손님이 메뉴를 시키는 것으로, 배달 주문, 포장 주문, 매장 주문이 가능하다.  |
|숨겨진 메뉴 | undisplayed menu  |  - 손님이 입력한 배달 주소로 배달 대행사를 통해 배달해주는 주문.  |
|배달 대행사 | delivery rider  |  - 배달 주소가 있어야 하며, 주문 후 전체 또는 부분 취소가 불가능하다.  |
|주문 상태  | order status  |  - 손님이 매장에 방문하여 포장해가는 주문.  |
|서빙 완료  | served  |  - 주문 후 전체 또는 부분 취소가 불가능하다.  |

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
