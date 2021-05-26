# Implement shopping cart
We will continue working on our Cinema project.

- Create models
    - ShoppingCart
    - Ticket
- Create DAO
    - ShoppingCartDao
        ```java
        public interface ShoppingCartDao {
            ShoppingCart add(ShoppingCart shoppingCart);
        
            ShoppingCart getByUser(User user);
        
            void update(ShoppingCart shoppingCart);
        }
        ```
    - TicketDao. Hint: use this dao in the ShoppingCartService, method addSession
        ```java
        public interface TicketDao {
            Ticket add(Ticket ticket);
        }
        ```   
- Create service
    - TicketService is not required. TicketDao is enough.
    - ShoppingCartService
        ```java
        public interface ShoppingCartService {
            /**
             * This method is responsible for adding a Ticket to the ShoppingCart
             * @param movieSession contains the information required for the ticket
             * @param user - the User who wants to buy the ticket for a specific movieSession
             */
            void addSession(MovieSession movieSession, User user);
        
            ShoppingCart getByUser(User user);
        
            void registerNewShoppingCart(User user);
      
            void clear(ShoppingCart shoppingCart);
        }
        ```

__You can check yourself using this__ [checklist](https://mate-academy.github.io/jv-program-common-mistakes/hibernate/add-shopping-cart/hibernate-shopping-cart-hw)  
