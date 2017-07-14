(Proposed UX specification for https://phynti.com/basic)

# Create a free Phynti account in 90 seconds

| Your e-mail address:               | `____________________`  | |
| Choose your master passphrase:     | `____________________`  | (1) |
| 1st friend's e-mail:               | `____________________`  | (2) |
| 2nd friend's e-mail:               | `____________________`  | |
| 3rd friend's e-mail:               | `____________________`  | |

<button>Create account</button>

If you want additional choices, such as making your bank a *mandatory key holder*, please use the [custom setup][].

(1) Your master passphrase should consist of at least four words. It is **_not_** stored by Phynti. It is recoverable when two of your friends share their key fragments with you, when combined with a single-use SMS code sent to your phone.

(2) Your friends will receive an e-mail with instructions on how to store the key fragment Phynti shares with them. By design, Phynti does **_not_** store the key fragment in a way that allows Phynti to retrieve it if your friend should lose it.

[Create account]: #create
[Custom setup]: custom

---

To do: Add more content. Some tests below.

[Test button 1](http://www.google.com){: .btn}

<button name="button">Test button 2</button>

<button class="btn">Test button 3</button>
