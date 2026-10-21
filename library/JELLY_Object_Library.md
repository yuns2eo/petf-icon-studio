# JELLY ICON — OBJECT LIBRARY

## Purpose

Icons that already exist in the set. When a request matches one of these objects (by name or alias), reuse its **object description exactly** so the new image matches the existing icon's shape.

The description covers shape and parts only. Colors, motif, material, light, and background always come from the lock and version files.

- **Fixed version**: the object always uses this version unless the request explicitly names another one.
- **Any**: the object exists in both cat and dog versions; ask which one if the request does not say.

---

## Common

| Object | Aliases | Symbol | Object description |
|---|---|---|---|
| 쿠폰 | 쿠폰티켓 | `COUPON` | a coupon ticket with a perforated stub on the right and notched sides |
| 할인티켓 | 퍼센트, 할인권 | `%` | a tilted discount ticket with a stub, layered over a second teal ticket |
| 가격표 | 가격태그, 택 | `₩` | two overlapping price tags (one pink, one teal) hanging from a chrome key ring, each with a small barcode strip |
| 선물상자 | 선물, 기프트 | – | a cube gift box with a big glossy ribbon bow on top |
| 장바구니 | 바구니 | – | a chrome wire shopping basket with two pink handles |
| 쇼핑카트 | 카트 | – | a chrome wire shopping cart with a pink handle and teal wheels |
| 포인트코인 | 코인, 포인트 | `P` | a thick gold coin with an embossed letter P, optionally a small stack of coins behind (color exception: gold) |
| 하트코인 | 날개하트코인 | – | a thick coin with an embossed heart with a small wing, in pink or chrome silver |
| 택배상자 | 박스, 택배 | – | a closed kraft cardboard parcel box with tape on top and a small barcode label (color exception: kraft brown) |
| 지갑 | – | – | a stitched bifold wallet with a teal card peeking out and a snap button (one paw allowed) |
| 말풍선 | 채팅, 리뷰 | – | a white rounded speech bubble with a glossy pink heart in the center |
| 종 | 알림, 벨 | – | a notification bell with a top loop and a clear glass clapper ball |
| 자명종 | 알람시계, 시계 | – | a twin-bell alarm clock with a white dial, teal bells and chrome legs and handle |
| 배송트럭 | 트럭, 배송 | – | a chubby delivery truck with a light pink cargo box and white bumper |
| 달력 | 캘린더, 출석 | `2026` | a desk flip calendar with chrome spiral rings, a pink header and a curled white page |
| 발바닥 | 발자국, 젤리발바닥 | – | a standalone paw print made of four glossy toe beans and one main pad, no base |

## Any (cat or dog)

| Object | Aliases | Object description |
|---|---|---|
| 사료그릇 | 밥그릇, 그릇 | a round pet food bowl filled with kibble |
| 사료캔 | 캔, 습식캔, 통조림 | an open wet food can with the peeled lid curled up, filled with shredded meat |
| 사료봉투 | 사료, 지퍼백, 파우치 | a stand-up zipper food pouch with a clear window showing kibble |
| 간식통 | 사료통, 트릿통 | a clear cylindrical jar with a colored lid, filled with treats |
| 자동급식기 | 급식기 | an automatic feeder with a clear kibble hopper on top and a small bowl at the bottom |
| 급수기 | 정수기, 물그릇 | a round pet water fountain with a clear dome and water flowing |
| 이동장 | 캐리어, 켄넬 | a pet carrier with a top handle, side vent slots and a front chrome grill door with a cushion inside |
| 빗 | 브러시, 슬리커 | a slicker grooming brush with a long handle and fine metal pins |
| 분무기 | 스프레이 | a clear spray bottle with a colored trigger head and a label |
| 방석 | 쿠션, 침대 | a round bolster pet bed with a cream plush cushion inside |
| 양치세트 | 칫솔, 치약 | a pet toothbrush with a round head standing in front of a toothpaste tube, both facing the same direction |

## Cat (fixed)

| Object | Aliases | Object description |
|---|---|---|
| 낚싯대 | 깃털장난감 | a cat wand toy with a handle, thin line and white feathers |
| 화장실 | 모래화장실 | an open rectangular litter box filled with sand |
| 캣타워 | 타워 | a small cat tower with a round hideout house, two sisal-rope posts, two round platforms and a dangling pompom |

## Dog (fixed)

| Object | Aliases | Object description |
|---|---|---|
| 간식볼 | 노즈워크볼, 트릿볼 | a clear treat-dispensing ball with holes and kibble inside |
| 리드줄 | 자동줄, 목줄 | a retractable leash handle with a chrome snap hook |

---

## Reference image map

Every registered icon has a front image in `references/{version}/{File}_Front.png`. Attach the matching file whenever the object appears in a request, alone or inside a combination.

| Version | Object → File |
|---|---|
| common | 쿠폰 → `Coupon_Pink` (teal: `Coupon_Teal`), 할인티켓 → `Discount_Ticket`, 가격표 → `Price_Tags`, 선물상자 → `Gift_Box`, 장바구니 → `Shopping_Basket`, 쇼핑카트 → `Shopping_Cart`, 포인트코인 → `Point_Coin`, 하트코인 → `Heart_Coin_Silver` / `Heart_Coin_Pink`, 택배상자 → `Parcel_Box`, 지갑 → `Wallet`, 말풍선 → `Speech_Bubble`, 종 → `Bell`, 자명종 → `Alarm_Clock`, 배송트럭 → `Delivery_Truck`, 달력 → `Calendar`, 발바닥 → `Paw` |
| cat | 사료그릇 → `Food_Bowl`, 사료캔 → `Food_Can_1` / `Food_Can_2`, 사료봉투 → `Food_Pouch`, 간식통 → `Food_Jar_1` / `Food_Jar_2`, 자동급식기 → `Auto_Feeder`, 급수기 → `Water_Fountain`, 이동장 → `Carrier`, 빗 → `Slicker_Brush`, 분무기 → `Spray_Bottle`, 낚싯대 → `Wand_Toy`, 화장실 → `Litter_Box`, 캣타워 → `Cat_Tower` |
| dog | 사료그릇 → `Food_Bowl`, 사료캔 → `Food_Can`, 사료봉투 → `Food_Pouch`, 간식통 → `Treat_Jar`, 간식볼 → `Treat_Ball`, 리드줄 → `Leash`, 방석 → `Bed`, 양치세트 → `Toothbrush_Set` |
| characters | 몽실이 → `Mongsil`, 방실이 → `Bangsil` |

Note: `Coupon_Pink` and `Coupon_Teal` are sheets of four coupon poses; use them for the coupon's shape and color only and still draw a single coupon.

A version that has no file for an object (e.g. a dog litter box) uses the other version's file for **shape only**, with this version's colors and motif.

---

## Adding a new object

When a new icon is finalised, add one row to the matching table:

- object name in Korean, 1–3 aliases
- symbol only if the object is defined by one
- one English sentence describing shape and parts only (no color, material, light, or background words)
