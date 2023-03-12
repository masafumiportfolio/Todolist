import tkinter as tk

tasks = []

def add_task():
    new_task = task_entry.get()
    tasks.append(new_task)
    task_entry.delete(0, tk.END)
    update_tasks()

def remove_task():
    task_index = task_listbox.curselection()
    if task_index:
        tasks.pop(task_index[0])
        update_tasks()

def update_tasks():
    task_listbox.delete(0, tk.END)
    for task in tasks:
        task_listbox.insert(tk.END, task)

root = tk.Tk()
root.title("ToDo List")

task_label = tk.Label(root, text="タスクを入力してください")
task_label.pack()

task_entry = tk.Entry(root, width=50)
task_entry.pack()

add_button = tk.Button(root, text="追加", command=add_task)
add_button.pack()

remove_button = tk.Button(root, text="削除", command=remove_task)
remove_button.pack()

task_listbox = tk.Listbox(root, height=10, width=50)
task_listbox.pack()

update_tasks()

root.mainloop()
