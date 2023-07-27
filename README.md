- 👋 Hi, I’m @denice-001
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---#include <iostream>
#include <vector>
#include <string>
#include <iomanip>

struct Item {
    std::string name;
    double price;
    int quantity;

    Item(const std::string& n, double p, int q) : name(n), price(p), quantity(q) {}
};

class PointOfSale {
private:
    std::vector<Item> catalog;
    std::vector<Item> cart;

public:
    PointOfSale() {
        // Sample items in the catalog
        catalog.push_back(Item("Hammer", 15.0, 10));
        catalog.push_back(Item("Screwdriver", 8.5, 15));
        catalog.push_back(Item("Wrench", 12.0, 20));
        catalog.push_back(Item("Pliers", 10.0, 12));
        catalog.push_back(Item("Tape Measure", 7.0, 18));
    }

    void displayCatalog() {
        std::cout << "Catalog:\n";
        for (const auto& item : catalog) {
            std::cout << item.name << "\t" << item.price << "\tAvailable: " << item.quantity << "\n";
        }
        std::cout << "\n";
    }

    void addItemToCart(const std::string& itemName, int quantity) {
        for (auto& item : catalog) {
            if (item.name == itemName) {
                if (item.quantity >= quantity) {
                    item.quantity -= quantity;
                    cart.push_back(Item(itemName, item.price, quantity));
                    std::cout << quantity << " " << itemName << "(s) added to cart.\n";
                } else {
                    std::cout << "Insufficient stock for " << itemName << ". Available: " << item.quantity << "\n";
                }
                return;
            }
        }
        std::cout << "Item not found in catalog.\n";
    }

    double calculateTotal() {
        double total = 0;
        for (const auto& item : cart) {
            total += item.price * item.quantity;
        }
        return total;
    }

    void printReceipt() {
        std::cout << "Receipt:\n";
        for (const auto& item : cart) {
            std::cout << item.name << "\t" << item.price << "\t" << item.quantity << "\n";
        }
        std::cout << "Total:\t" << std::fixed << std::setprecision(2) << calculateTotal() << "\n";
    }

    void recordTransaction() {
        // In a real-world application, you would save transaction details to a database or file.
        // This function is a placeholder to demonstrate recording transactions.
        std::cout << "Transaction recorded.\n";
    }
};

int main() {
    PointOfSale pos;

    std::cout << "Welcome to the Hardware Store Point of Sale Terminal!\n";

    char choice;
    do {
        pos.displayCatalog();

        std::string itemName;
        int quantity;

        std::cout << "Enter the item name: ";
        std::cin >> itemName;

        std::cout << "Enter the quantity: ";
        std::cin >> quantity;

        pos.addItemToCart(itemName, quantity);

        std::cout << "Do you want to continue shopping? (y/n): ";
        std::cin >> choice;
    } while (choice == 'y' || choice == 'Y');

    pos.printReceipt();
    pos.recordTransaction();

    return 0;
}

denice-001/denice-001 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
