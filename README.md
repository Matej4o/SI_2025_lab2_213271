# SI_2025_lab2_213271

## Матеј Филиповски, 213271

### CFG:
![SILab2 drawio](https://github.com/user-attachments/assets/5d33f82f-8d01-4419-88f7-274756fe6515)

### Цикломатска комплексност:  
Формулата е V(G) = E - N + 2P  
- Број на јазли (N): 19
- Број на рабови (E): 28
- Број на компоненти (P): 1
Формула: V(G) = E - N + 2P = 28 - 19 + 2 = **11**

### Тест случаи - Every Statement:

1. **allItems == null**  
   - Покрива throw за невалидна листа
2. **Валиден предмет со попуст и валидна картичка**  
   - Покрива нормален тек на извршување (discount, loop, return)
3. **Невалиден предмет (name == null)**  
   - Покрива throw при невалиден item


### Тест случаи - Multiple Conditions:

if (item.getPrice() > 300 || item.getDiscount() > 0 || item.getQuantity() > 10)

Тестирани се сите можни комбинации на подусловите:
- A: price > 300  
- B: discount > 0  
- C: quantity > 10  

Тест | A | B | C | Очекувано  
TC1  | F | F | F | НЕ се одзема 30  
TC2  | F | F | T | Се одзема 30  
TC3  | F | T | F | Се одзема 30  
TC4  | F | T | T | Се одзема 30  
TC5  | T | F | F | Се одзема 30  
TC6  | T | F | T | Се одзема 30  
TC7  | T | T | F | Се одзема 30  
TC8  | T | T | T | Се одзема 30  

Овие тестови обезбедуваат целосна Multiple Condition покриеност за дадениот услов.
