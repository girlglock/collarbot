# collarbot moderator guide

## adding & removing commands
- **add a command:**  
  ```
  !addcollar <commandname> <response>
  ```
- **remove a command:**  
  ```
  !removecollar <commandname>
  ```

### variables
- `{user}` - username of the person who used the command  
- `{args}` - all arguments after the command  
- `{arg1}`, `{arg2}`, etc. - individual arguments  

---

## benchmark commands

**basic benchmark command:**
```
!addcollar bench {bench:{args}}
```
<details>
<summary>usage & response</summary>

- **usage:** `!bench somesteamvanity viscose easier`  
- **response:** `someplayer is ranked as seal (92.66%) on viscose benchmarks (easier)`

</details>

---

### command setup examples

**complete preset command:**
```
!addcollar viscoseeasy {bench:somesteamvanity viscose easier}
```
<details>
<summary>usage & response</summary>

- **usage:** `!viscoseeasy`  
- **response:** `someplayer is ranked as seal (92.66%) on viscose benchmarks (easier)`

</details>

**generic benchmark command:**
```
!addcollar bench {bench:{args}}
```
<details>
<summary>usage & response</summary>

- **usage:** `!bench somesteamvanity viscose easier`  
- **response:** `someplayer is ranked as seal (92.66%) on viscose benchmarks (easier)`

</details>

**fixed player, selectable difficulty:**
```
!addcollar viscose {bench:somesteamvanity viscose {arg1}}
```
<details>
<summary>usage & response</summary>

- **usage:** `!viscose medium`  
- **response:** `someplayer is ranked as iron (15.23%) on viscose benchmarks (medium)`

</details>

---

## random commands

**random number:**
```
!addcollar dice {user} rolled a {random:1:6}!
```
<details>
<summary>usage & response</summary>

- **usage:** `!dice`  
- **response:** `alice rolled a 4!`

</details>

**daily random number:**
```
!addcollar dailyscore today's stream score: {randomdaily:1:10}/10
```
<details>
<summary>usage & response</summary>

- **usage:** `!dailyscore`  
- **response:** `today's stream score: 7.42/10`

</details>

**random item:**
```
!addcollar weapon your weapon: {randomitem:[sword,bow,staff,dagger]}
```
<details>
<summary>usage & response</summary>

- **usage:** `!weapon`  
- **response:** `your weapon: bow`

</details>

**daily random item:**
```
!addcollar fortune today's fortune: {randomitemdaily:[great,good,okay,bad,terrible]}
```
<details>
<summary>usage & response</summary>

- **usage:** `!fortune`  
- **response:** `today's fortune: good`

</details>

---

## time & math commands

**countdown timer:**
```
!addcollar newyear new year countdown: {countdown:01.01.25 12am gmt}
```
<details>
<summary>usage & response</summary>

- **usage:** `!newyear`  
- **response:** `new year countdown: 15d 6h 23m`

</details>

**math calculator:**
```
!addcollar calc result of {args}: {math:{args}}
```
<details>
<summary>usage & response</summary>

- **usage:** `!calc 5*8+12`  
- **response:** `result of 5*8+12: 52`

</details>

**fetch data:**
```
!addcollar weather current weather: {fetch:https://wttr.in/?format=3}
```
<details>
<summary>usage & response</summary>

- **usage:** `!weather`  
- **response:** `current weather: london: ☁️ +15°c`

</details>

---

## permissions
only **moderators** and the **broadcaster** can add or remove commands.
