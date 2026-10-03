def find_common_prefix(words):
    if not words:
        return ""

    prefix = words[0]

    for word in words[1:]:
        while not word.startswith(prefix):
            prefix = prefix[:-1]

            if not prefix:
                return ""

    return prefix


if __name__ == "__main__":
    words = ["github", "git", "gift", "giga"]

    print("Words:", words)
    print("Common prefix:", find_common_prefix(words))
