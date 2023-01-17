# learn-swift
Follow my progress as I learn swift for application development

#Example of code using for loops to create a cipher using the famous Caesar Cipher method

var alphabet: [Character] = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z"]

var secretMessage = "Why does this work"

var message = Array(secretMessage)

// print(message)

for i in 0..<message.count {
  for j in 0..<alphabet.count {
    if message[i] == alphabet[j] {

      message[i] = alphabet[(j+3) % 26]
      break

    }
  }
}

var finalMessage = String(message).lowercased()

print(finalMessage)
