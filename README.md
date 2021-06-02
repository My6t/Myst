# Svoya Igra
- данный репозиторий, содержит код и прочие ресурсы игры "Svoya Igra" *(временное название)*.
Проект разрабатывается на игровом движке Unity (сайт движка: https://unity.com/) на языке C#.

### Пример содержимого репозитория:

Пример кода:
```csharp
using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;
using UnityEngine.UI;
using System;
using UnityEngine.EventSystems;
using UnityEditor;
using Photon.Pun.UtilityScripts;

public class RedactorManager : MonoBehaviour
{
    public RectTransform TopicButtonPrefab;
    public RectTransform QuestionButtonPrefab;
    public RectTransform ScreenPanelPrefab;
    public RectTransform contentScrollPanel;

    public Slider TopicSlider;
    public Slider QuestionSlider;

    public GameObject GridSizePanel;
    public GameObject ScrollPanel;
    public GameObject LeftArrow;
    public GameObject RightArrow;
    public GameObject TextQuestionPanel;
    public GameObject MusicQuestionPanel;
    public GameObject VideoQuestionPanel;
    public GameObject PictureQuestionPanel;
    public GameObject DropDown;

    public InputField TopicInputField;
    public InputField QuestionInputField;

    public float speed;

    public string previousButtonName = "";

    int iconst = 0;
    int countofRound = 0;
    int currentRound = 0;

    //Подставляем числовое значение слайдера темы в текстовое поле темы
    public void TopicValueChange()
    {
        TopicInputField.text = TopicSlider.value.ToString();
    }

    //Переводим введенный текст в текстовое поле темы в числовое значение слайдера темы
    public void TopicInputFieldChange()
    {
        TopicSlider.value = Int32.Parse(TopicInputField.text);
    }

    //Подставляем численное значение слайдера вопроса в текстовое поле вопроса
    public void QuestionValueChange()
    {
        QuestionInputField.text = QuestionSlider.value.ToString();
    }

    //Переводим введенный текст в текстовое поле вопроса в числовое значение слайдера вопроса
    public void QuestionInputFieldChange()
    {
        QuestionSlider.value = Int32.Parse(QuestionInputField.text);
    }

    //При нажатии на кнопку "новый раунд" становится активной панель выбора размера сетки
    public void NewRoundButtonClicked()
    {
        GridSizePanel.SetActive(true);
    }
```

Пример интерфейса:
![Image](https://github.com/My6t/Myst/blob/master/%D0%9A%D0%BE%D0%BD%D1%86%D0%B5%D0%BF%D1%82%20%D1%80%D0%B5%D0%B4%D0%B0%D0%BA%D1%82%D0%BE%D1%80%D0%B0%20%D0%BF%D0%B0%D0%BA%D0%BE%D0%B2.png?raw=true)

## На какой стадии разработки находится проект?
Проект заброшен(:poop:)
