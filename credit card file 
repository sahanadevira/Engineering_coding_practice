def validate_card(card):

    if "-" in card:
        parts = card.split("-")

        if len(parts) != 4:
            return "Invalid"

        for p in parts:
            if len(p) != 4 or not p.isdigit():
                return "Invalid"

        card = "".join(parts)

    else:
        if len(card) != 16 or not card.isdigit():
            return "Invalid"

    if card[0] not in ['4','5','6']:
        return "Invalid"

    count = 1
    for i in range(1, len(card)):
        if card[i] == card[i-1]:
            count += 1
            if count == 4:
                return "Invalid"
        else:
            count = 1

    return "Valid"


n = int(input())

for i in range(n):
    card = input()
    print(validate_card(card))
