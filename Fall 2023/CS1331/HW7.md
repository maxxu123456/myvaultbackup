```java
/**
 * @author Max Xu
 * @version 1.0
 */
public class Restaurant {
    /**
     * @param rolls list of sushi rolls
     * @return returns a sorted arry of sushi rolls
     */
    public static SushiRoll[] mergeSortRolls(SushiRoll[] rolls) {
        if (rolls.length == 0) {
            return rolls;
        }
        if (rolls.length == 1) {
            return rolls;
        }
        int mid = rolls.length / 2;
        SushiRoll[] arr1 = RecursionUtils.copyOfRange(rolls, 0, mid);
        SushiRoll[] arr2 = RecursionUtils.copyOfRange(rolls, mid, rolls.length);

        arr1 = mergeSortRolls(arr1);
        arr2 = mergeSortRolls(arr2);

        return RecursionUtils.merge(arr1, arr2);
    }

    /**
     * @param orders list of orders to be merged
     * @return merged orders that are sorted
     */

    public static SushiRoll[] mergeOrders(SushiRoll[][] orders) {
        if (orders.length == 0) {
            return new SushiRoll[0];
        }
        return mergeOrdersRun(orders, 0);

    }

    /**
     * @param orders list of orders to the merged
     * @param i      index
     * @return returns merged and sorted orders
     */
    public static SushiRoll[] mergeOrdersRun(SushiRoll[][] orders, int i) {
        if (i >= orders.length) {
            return new SushiRoll[0];
        }
        SushiRoll[] others = mergeOrdersRun(orders, i + 1);
        return RecursionUtils.merge(orders[i], others);
    }

    /**
     * @param rolls list of sushi rolls
     * @param c     color
     * @return returns sushi rolls with color
     */
    public static SushiRoll[] platesOfColor(SushiRoll[] rolls, Color c) {
        return platesOfColorRun(rolls, c, 0);
    }

    /**
     * @param rolls list of sushi rolls
     * @param c     color
     * @param i     index
     * @return returns sushi rolls with color
     */
    public static SushiRoll[] platesOfColorRun(SushiRoll[] rolls, Color c, int i) {
        if (i >= rolls.length) {
            return new SushiRoll[0];
        }
        if (rolls[i].getColor() == c) {
            SushiRoll[] curr = new SushiRoll[] {rolls[i]};
            SushiRoll[] other = platesOfColorRun(rolls, c, i + 1);
            return RecursionUtils.merge(curr, other);
        }
        return platesOfColorRun(rolls, c, i + 1);
    }

    /**
     * @param rolls list of sushi rolls
     * @return returns total price of sush rolls
     */
    public static double totalPrice(SushiRoll[] rolls) {
        if (rolls.length == 0) {
            return 0.0;
        }
        if (rolls.length == 1) {
            return rolls[0].getColor().getPrice();
        }
        return rolls[0].getColor().getPrice() + totalPrice(RecursionUtils.copyOfRange(rolls, 1, rolls.length));
    }

    /**
     * @param rolls sushi rolls
     */
    public static void flip(SushiRoll[] rolls) {
        if (rolls.length == 0 || rolls.length == 1) {
            return;
        }
        flipRun(rolls, 0, rolls.length - 1);
    }

    /**
     * @param rolls sushi rolls
     * @param i     index of start
     * @param j     index of end
     */
    public static void flipRun(SushiRoll[] rolls, int i, int j) {
        if (i > j) {
            return;
        }
        SushiRoll temp = rolls[i];
        rolls[i] = rolls[j];
        rolls[j] = temp;
        flipRun(rolls, i + 1, j - 1);
    }
}
```