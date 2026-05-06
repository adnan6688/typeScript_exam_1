Question 03 : How do Generics allow you to build reusable components and functions that stay strictly typed regardless of the data structures passed in?


Title: Generics in TypeScript: Reusable and Type-Safe Code

Introduction:
Generics holo TypeScript-er ekta powerful feature ja tomake reusable function ebong component banate help kore, and same time-e strict typing maintain kore. Eitar maddhome tumi large-scale project-e flexibility and safety duita-i paba.

Body:

Generic Function Example:

function identity<T>(value: T): T {
  return value;
}

const num = identity<number>(10);
const str = identity<string>("hello");

Ekhane T jekono type hote pare, but return type same thake → eta type safety ensure kore.

Reusable Component Logic:

function getFirstItem<T>(arr: T[]): T {
  return arr[0];
}

const first = getFirstItem<string>(["a", "b", "c"]);

Same function different data structure-e kaj kortese → code reuse baray.

Using Constraints:

function getLength<T extends { length: number }>(item: T): number {
  return item.length;
}

Ekhane constraint use kore ensure kora hoise je passed data-te length property thakte hobe.

Conclusion:
Generics use korle tumi ekbar code likhe multiple type handle korte parba, and strict typing o maintain thakbe. Eita code ke aro reusable, maintainable, and scalable kore.