# my-first-repo
just testing github
# guess_number.py
import random

print("🎯 بازی حدس عدد 🎯")
print("من یک عدد بین 1 تا 20 انتخاب کردم، سعی کن حدسش بزنی!")

# انتخاب عدد تصادفی
secret_number = random.randint(1, 20)
attempts = 0

while True:
    guess = input("حدس شما: ")

    if not guess.isdigit():
        print("لطفاً یک عدد معتبر وارد کنید.")
        continue

    guess = int(guess)
    attempts += 1

    if guess < secret_number:
        print("بزرگ‌تر...")
    elif guess > secret_number:
        print("کوچک‌تر...")
    else:
        print(f"✅ آفرین! عدد {secret_number} رو در {attempts} تلاش پیدا کردی!")
        break
