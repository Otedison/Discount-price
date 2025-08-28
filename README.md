# Discount-price
def calculate_discount(price, discount_percent):
    """
    Calculate the final price after applying a discount.
    
    Parameters:
    price (float): Original price of the item
    discount_percent (float): Discount percentage (0-100)
    
    Returns:
    float: Final price after discount (if applicable)
    """
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price

# Main program to interact with user
def main():
    try:
        # Prompt user for input
        original_price = float(input("Enter the original price of the item: $"))
        discount_percentage = float(input("Enter the discount percentage: "))
        
        # Calculate final price
        final_price = calculate_discount(original_price, discount_percentage)
        
        # Display results
        print(f"\nOriginal price: ${original_price:.2f}")
        print(f"Discount percentage: {discount_percentage}%")
        
        if discount_percentage >= 20:
            discount_amount = original_price * (discount_percentage / 100)
            print(f"Discount amount: ${discount_amount:.2f}")
            print(f"Final price after {discount_percentage}% discount: ${final_price:.2f}")
        else:
            print("No discount applied (discount must be 20% or higher)")
            print(f"Final price: ${final_price:.2f}")
            
    except ValueError:
        print("Error: Please enter valid numbers for price and discount percentage.")

# Run the program
if __name__ == "__main__":
    main()

Example

    Enter the original price of the item: $100
Enter the discount percentage: 25

Original price: $100.00
Discount percentage: 25%
Discount amount: $25.00
Final price after 25% discount: $75.00


Enter the original price of the item: $50
Enter the discount percentage: 15

Original price: $50.00
Discount percentage: 15%
No discount applied (discount must be 20% or higher)
Final price: $50.00
