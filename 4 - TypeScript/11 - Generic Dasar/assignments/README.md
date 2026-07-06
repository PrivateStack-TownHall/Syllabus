# Tujuan Pembelajaran
- Memahami konsep generic dan alasan penggunaannya
- Mampu membuat function generic
- Mampu membuat interface dan class generic
- Memahami generic constraint

---

# Assignment 1 - Function Generic Sederhana (Easy)
Buat function generic yang mengembalikan nilai apapun sesuai tipe input-nya.

```ts
function identitas<T>(value: T): T {
  return value;
}

console.log(identitas<string>("Vincent"));
console.log(identitas<number>(25));
```

**Hasil yang diharapkan:**
```
Vincent
25
```

---

# Assignment 2 - Generic pada Array (Easy)
Buat function generic untuk mengembalikan elemen pertama dari sebuah array.

```ts
function elemenPertama<T>(arr: T[]): T {
  return arr[0];
}

console.log(elemenPertama<number>([10, 20, 30]));
console.log(elemenPertama<string>(["Ani", "Budi"]));
```

**Hasil yang diharapkan:**
```
10
Ani
```

---

# Assignment 3 - Generic dengan Dua Parameter (Easy)
Buat function generic yang menggabungkan dua nilai dengan tipe berbeda menjadi sebuah tuple.

```ts
function gabungkanPasangan<T, U>(a: T, b: U): [T, U] {
  return [a, b];
}

console.log(gabungkanPasangan<string, number>("Vincent", 25));
```

**Hasil yang diharapkan:**
```
[ 'Vincent', 25 ]
```

---

# Assignment 4 - Generic Interface (Easy)
Buat interface generic `Kotak<T>` untuk menyimpan nilai apapun.

```ts
interface Kotak<T> {
  isi: T;
}

let kotakAngka: Kotak<number> = { isi: 100 };
let kotakString: Kotak<string> = { isi: "Sekolah Stack" };

console.log(kotakAngka, kotakString);
```

**Hasil yang diharapkan:**
```
{ isi: 100 } { isi: 'Sekolah Stack' }
```

---

# Assignment 5 - Generic Type Alias (Easy)
Buat type alias generic `Respons<T>` untuk merepresentasikan response API sederhana.

```ts
type Respons<T> = {
  success: boolean;
  data: T;
};

let respons1: Respons<string> = { success: true, data: "Berhasil disimpan" };

console.log(respons1);
```

**Hasil yang diharapkan:**
```
{ success: true, data: 'Berhasil disimpan' }
```

---

# Assignment 6 - Generic Class (Medium)
Buat class generic `Stack<T>` sederhana dengan method push dan pop.

```ts
class Stack<T> {
  private items: T[] = [];

  push(item: T): void {
    this.items.push(item);
  }

  pop(): T | undefined {
    return this.items.pop();
  }
}

let stackNumber = new Stack<number>();
stackNumber.push(1);
stackNumber.push(2);

console.log(stackNumber.pop());
```

**Hasil yang diharapkan:**
```
2
```

---

# Assignment 7 - Generic Constraint (Medium)
Buat function generic dengan constraint agar parameter yang diterima wajib memiliki properti `length`.

```ts
interface MemilikiLength {
  length: number;
}

function tampilkanPanjang<T extends MemilikiLength>(item: T): number {
  return item.length;
}

console.log(tampilkanPanjang("Sekolah Stack"));
console.log(tampilkanPanjang([1, 2, 3, 4]));
```

**Hasil yang diharapkan:**
```
13
4
```

---

# Assignment 8 - Generic dengan Default Type (Hard)
Buat generic interface `Respons<T = string>` dengan default type parameter, lalu gunakan tanpa dan dengan menentukan tipe secara eksplisit.

```ts
interface Respons<T = string> {
  success: boolean;
  data: T;
}

let respons1: Respons = { success: true, data: "OK" };
let respons2: Respons<number[]> = { success: true, data: [1, 2, 3] };

console.log(respons1);
console.log(respons2);
```

**Hasil yang diharapkan:**
```
{ success: true, data: 'OK' }
{ success: true, data: [ 1, 2, 3 ] }
```
