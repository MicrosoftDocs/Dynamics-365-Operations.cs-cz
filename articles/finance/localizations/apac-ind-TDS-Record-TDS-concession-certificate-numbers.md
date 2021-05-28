---
title: Zaznamenání čísel koncesních certifikátů TDS
description: Toto téma vysvětluje, jak zaznamenat čísla koncesních certifikátů daně odečtené u zdroje (TDS), která jsou vydávána prodejcům.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023076"
---
# <a name="record-tds-concession-certificate-numbers"></a>Zaznamenání čísel koncesních certifikátů TDS

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak zaznamenat čísla koncesních certifikátů daně odečtené u zdroje (TDS), která jsou vydávána prodejcům.

1. Přejděte na **Daň \> Nepřímé daně \> Srážková daň \> Koncese srážkové daně**.
2. V poli **Typ daně** vyberte **TDS** k zaznamenání koncesních certifikátů pro daňový typ TDS.
3. Na kartě **Přehled** vyberte **Alt + N** k vytvoření řádku.

    [![Záhlaví nového řádku](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. V poli **Kód srážkové daně** vyberte daňový kód TDS, pro který jsou vydány koncesní certifikáty dodavatele. Pole **Název srážkové daně** zobrazuje název kódu daně TDS.
5. V polích **Od data** a **Do data** definujte dobu platnosti koncesního certifikátu, který používá daňový kód TDS k výpočtu TDS koncesně.
6. Do pole **Poznámky** zadejte jakékoli poznámky.
7. V poli **Oddíl** zadejte kód oddílu zákona, pod kterým je koncesní certifikát TDS vydáván.

    Pokud je kód oddílu 197, hodnota „A“ se objeví ve sloupci „Důvod pro neodpočítávání / nižší odpočet“ ve formuláři 26Q a ve sloupci „Důvod pro neodpočítávání / nižší odpočet / přepočítání (pokud existuje)“ ve formulářu 27Q. Pokud je kód sekce 197A, zobrazí se na obou těchto místech hodnota „B“.

8. Vyberte pevnou kartu **Certifikát** pro záznam čísel koncesních certifikátů TDS pro dodavatele.
9. V poli **Účet dodavatele** vyberte účet dodavatele, pro který je vydán koncesní certifikát TDS.
10. V polích **Od data** a **K datu** definujte dobu platnosti koncesního certifikátu TDS.

    Výpočet TDS na základě zvýhodnění je založen na období, kdy je certifikát pro dodavatele vytvořen.

11. Do pole **Certifikát** zadejte číslo koncesního certifikátu TDS.

    [![Pevná záložka Certifikát](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Zavřete stránku.
