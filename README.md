def fix_dictionary(file1, file2):
    with open(file1, "r") as f:
        lines = f.readlines()

    fixed_lines = []

    for line in lines:
        line = line.replace("=", ":")
        line = line.replace("?", ":")
        fixed_lines.append(line)

    with open(file2, "w") as f:
        f.writelines(fixed_lines)
