# UnderTheGravestone
- это приватный репозиторий, содержащий код и прочие ресурсы игры "Under The Gravestone" *(название рабочее)*.
Проект разрабатывается на игровом движке Unity Engine 5 (сайт движка: https://unity.com/) на языке C#.

### Репозиторий содержит:
* файлы кода;
* графические ресурсы;
* специальные объекты движка (ScriptableObject's, некоторые meta-файлы, и т.д.);
* текст;
* анимационные клипы и т.д.

### Примеры содержимого репозитория:

Пример кода:
```csharp
using UnityEngine;
using UnityEngine.Experimental.Rendering.Universal;
using StateMachine;

namespace Scripts
{
public class StreetlightTurnOnState : State, IOnUpdate
{
[SerializeField] private Light2D shineLight;
[SerializeField, Range(0f, 0.2f)] private float flickerRange = .1f;

private float defaultIntensity;
private float minFlicker, maxFlicker;

protected override void OnEnter()
{
this.defaultIntensity = this.shineLight.intensity;
this.minFlicker = this.defaultIntensity - this.flickerRange;
this.maxFlicker = this.defaultIntensity + this.flickerRange;
}

public void OnUpdate()
{
this.shineLight.intensity = Random.Range(this.minFlicker, this.maxFlicker);
}

protected override void OnExit()
{
this.shineLight.intensity = this.defaultIntensity;
}
}
}
```

Пример графического ресурса:
![Image](https://github.com/StupidMoth/UnderTheGravestone/blob..)

## На какой стадии разработки находится проект?
Начальной :)

## Кто занимается разработкой игры?
Разработкой занимаются 3 человека, среди них:
* Я - в качестве программиста;
* Olisa - в качестве художника и сценариста;
* TheKatya - в качестве худоника.