def show_message(action, note):
    match action:
        case "add":
            print(f"Заметка добавлена: {note}")
        case "edit":
            print(f"Заметка изменена: {note}")
        case "delete":
            print(f"Заметка удалена: {note}")
        case _:
            print("Неизвестное действие")


def show_collection(notes):
    print("Список заметок:")
    for i, note in enumerate(notes, 1):
        print(f"{i}. {note}")


def test():
    notes = ["Купить хлеб", "Сделать ДЗ"]

    show_message("add", "Позвонить другу")
    show_message("edit", "Сделать ДЗ")
    show_message("delete", "Купить хлеб")

    show_collection(notes)


test()
