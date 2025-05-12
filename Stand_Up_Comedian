import flet as ft
import random

jokes = [
    "Why did the scarecrow win an award? Because he was outstanding in his field!",
    "Why don't skeletons fight each other? They don't have the guts!",
    "Why was the math book sad? It had too many problems!",
    "Why did the golfer bring two pairs of pants? In case he got a hole in one!",
    "Why can't a nose be 12 inches long? Because then it would be a foot!",
    "Why did the bicycle fall over? It was two-tired!",
    "Why did the tomato turn red? Because it saw the salad dressing!",
    "Why did the computer go to the doctor? It had a virus!",
    "Why did the coffee file a police report? It got mugged!",
    "Why did the chicken join a band? Because it had the drumsticks!"]

def main(page: ft.Page):
    def show_joke(e):
        joke = random.choice(jokes)
        bottom_sheet.content.controls[0].value = joke
        page.open(bottom_sheet)
        page.update()

    def close_bottom_sheet(e):
        page.close(bottom_sheet)
        page.update()

    bottom_sheet = ft.BottomSheet(
            content=ft.Column([
                ft.Text(""),
                ft.ElevatedButton("Close", on_click=close_bottom_sheet)
            ], alignment=ft.MainAxisAlignment.CENTER)
    )

    joke_button = ft.ElevatedButton("Tell me a joke", on_click=show_joke)
    

    page.add(joke_button)
ft.app(target=main)
