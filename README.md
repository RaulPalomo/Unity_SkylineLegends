
# Unity_SkylineLegends
En aquest repositori es troba el projecte de Unity del videojoc Skyline Legends, produit per David Sanz, Arnau Molano i Raúl Palomo.

## Funcionalitats del Videojoc
- **Pantalla dividida**: Competeix en local per veure qui és el millor pilot.
- **Carreres**: Recorre diferents carreres amb les teves naus.
- **Caixa misteriosa**: Desbloqueja les naus tirant una caixa misteriosa.

## Contingut
- **Scripts**  
  Els scripts es troben separats per carpetes que determinen la seva categoria:
  - **API**
  - **UI**
  - **Jugador**
  - **Mapa**
- **Assets**
- **Projecte executable en Unity**

## Tecnologies utilitzades
- **Coroutines**  
  Les coroutines són un mètode utilitzat a Unity per executar diferents línies de codi en paral·lel. Les hem utilitzat per recuperar dades de l'API, el moviment de les naus, controlar animacions i altres funcions.
  ~~~
 	public void Boost()
	{
		if (!isBoosting)
		{
			StartCoroutine(BoostSpeed());
           
        }
	}
  ~~~
  ~~~
  public IEnumerator BoostSpeed()
  {
  
	isBoosting = true;
	float auxSpeed = maxSpeed;
	maxSpeed = boostSpeed;
	float duration = 1.0f;
	float elapsedTime = 0.0f;

	float initialSpeed = Speed;
	float initialAcceleration = acceleration;

	Speed = boostSpeed;
	acceleration = 0;

	Debug.Log($"Boost started: Speed={Speed}, Acceleration={acceleration}, ElapsedTime={elapsedTime}");

    

   	 while (elapsedTime < duration)
	{
		elapsedTime += Time.deltaTime;
		yield return null;
	}

	Speed = initialSpeed;
	acceleration = initialAcceleration;
	maxSpeed = auxSpeed;
	isBoosting = false;
   
  }
  ~~~
- **Llibreries Unity**  
Hem utilitzat diverses llibreries de Unity per a la creació del joc:
  - UnityEngine: La llibreria principal de Unity, utilitzada per accedir a les funcionalitats bàsiques del motor de joc.
  - UnityEngine.UI: Per a la creació i gestió d'interfícies d'usuari.
  - Cinemachine: Per a la gestió avançada de càmeres i efectes visuals.
- **Visual Studio Code Community**  
Hem treballat els nostres codis de Unity amb aquest IDE, ja que és amb el que estem més familiaritzats, té una gran compatibilitat amb Unity i proporciona eines per facilitar les tasques.

## Instruccions d'Ús
- Per obrir a unity: descarregar el zip del del link i afegir el projecte SkylineGame a unity.
- Per obrir el build: descarregar el build de github i execuutar la aplicació.
- Enllaç del Projecte:

## Contacte
- **David Sanz**: [david.sanz.7e7@itb.cat](mailto:david.sanz.7e7@itb.cat)
- **Arnau Molano**: [arnau.molano.7e7@itb.cat](mailto:arnau.molano.7e7@itb.cat)
- **Raúl Palomo**: [raul.palomo.7e7@itb.cat](mailto:raul.palomo.7e7@itb.cat)

