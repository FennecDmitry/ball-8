import random

answers = ['несомненно', 'это определенно так', 'без сомнения', 'да – наверняка', 'Ты можешь доверять ему',
           'Как я это вижу, да', 'скорее всего', 'лучше', 'да признаки указывают на да', 'Ответ туманный', 'снова',
           'я спрошу тебя еще раз позже.', 'Лучше не говорить тебе сейчас', 'Не могу предсказать сейчас', 'сконцентрируйся и спроси еще раз',
           'Не рассчитывай на это', 'Мой ответ - нет', 'Мои источники говорят, что нет', 'Перспективы не очень хорошие', 'Очень сомнительно']

print('  __  __          _____ _____ _____    ___  ')
print(' |  \/  |   /\   / ____|_   _/ ____|  / _ \ ')
print(' | \  / |  /  \ | |  __  | || |      | (_) |')
print(' | |\/| | / /\ \| | |_ | | || |       > _ < ')
print(' | |  | |/ ____ \ |__| |_| || |____  | (_) |')
print(' |_|  |_/_/    \_\_____|_____\_____|  \___/ ')
print('')
print('')
print('')
print('Hello World! Я шарик судьбы(´･ᴗ･ ), Как вас зовут?')
name = input()
print('hello ＼(￣▽￣)／ ' + name)


def Magic8Ball():
    print('Задай мне вопрос.')
    ask = input()
    if ask == "как дела?":
        print("Хорошо, спасибо что спросил ")
        Replay()
    else:
        print(answers[random.randint(0, len(answers) - 1)])
        print('Я надеюсь, что это помогло!!!')
        Replay()


def Replay():
    print('Есть другие вопросы? [Y/N] ')
    reply = input()
    if reply == 'Y':
        Magic8Ball()
    elif reply == 'N':
        exit()
    else:
        print('Прошу прощения, я этого не расслышал. Пожалуйста, повторите.')
        Replay()


Magic8Ball()
