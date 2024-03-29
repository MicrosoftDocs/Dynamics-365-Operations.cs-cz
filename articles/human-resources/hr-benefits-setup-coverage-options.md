---
title: Vytvoření možností pokrytí
description: Tento článek popisuje možnosti pokrytí v Microsoft Dynamics 365 Human Resources v plánu nebo programu zaměstnanecké výhody účastníka.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f9c107e31e58ba1302cd02e2e82aa405dda0fdef
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336898"
---
# <a name="create-coverage-options"></a>Vytvoření možností pokrytí


Možnosti krytí určují, kdo by měl být krytý, nebo kolik krytí je k dispozici v pojistném plánu. Například pro lékařský plán můžete mít možnost **Pouze zaměstnanec**, **Zaměstnanec + 1** a **Rodina**. U životního pojištění můžete nabídnout krytí pro **1 x plat** nebo **2 x plat**.

Po definování můžete znovu použít možnosti pokrytí zaměstnaneckých výhod. Můžete přidružit možnost k jednomu nebo více plánům.

> [!IMPORTANT]
> Po definování možností pokrytí připojte možnosti pokrytí k typu plánu zaměstnaneckých výhod. Typ plánu je poté přidružen k plánu zaměstnaneckých výhod nebo k programu. Možnosti disponibility, které jsou přidruženy k typu plánu, jsou dostupné pro všechny plány vytvořené s tímto typem plánu.

## <a name="create-coverage-options"></a>Vytvoření možností pokrytí
1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** **Možnosti pokrytí**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Možnost pokrytí** | Jedinečný název možnosti pokrytí. |
   | **Popis** | Popis možnosti pokrytí. |
   | **Kód pokrytí** | Kódy pokrytí přiřazují minimální a maximální částky každému typu osoby s nárokem na pokrytí. Kód pokrytí indikuje, kdo má pokrytí nebo jaká částka pokrytí je povolena pro daný typ plánu. Částku pokrytí lze vyjádřit jako částku v korunách nebo v procentech. Například:<ul><li>**Emp+1** – aby měl zaměstnanec nárok, musí mít vybranou jednu závislou osobu (pokud jich je vybráno více, nárok se ztrácí).</li><li>**Emp+family** – abyste mohl mít zaměstnanec nárok, musí mít vybrané nejméně dvě závislé osoby.</li></ul> |
   | **Maximální počet** | Maximální počet závislých osob |
   | **Stav** | Stav možnosti pokrytí. Je-li stav možnosti pokrytí nastaven na hodnotu **Neaktivní**, nelze pro typy plánů vybrat možnost Pokrytí. |
   | **Procento** | Procentuální částka. Toto pole je aktivní pouze v případě, že v poli kód disponibility byla vybrána možnost % x mzdy. |
   | **Dělitel** | Dělitel, který má být použit ve výpočtu po výběru kódu pokrytí % x platu. |
   | **Minimální procento** | Minimální procento, když vyberete kód procentuálního pokrytí. |
   | **Maximální procento** | Maximální procento, když vyberete kód procentuálního pokrytí. |

4. Ve skupinovém rámečku **Možnosti nároku na osobní kontakt** připojte ke každé možnosti nároku odpovídající osobní kontakty.

5. V části **Samoobsluha** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Povolit částku příspěvku zaměstnance** | Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku příspěvku na samoobslužné služby. Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky příspěvku, kterou zaměstnanec zadá v samoobsluze zaměstnaneckých výhod. |
   | **Povolit částku pokrytí zaměstnance** | Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku pokrytí na samoobslužné služby. Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky pokrytí, kterou zaměstnanec zadá do samoobsluhy zaměstnance. |

6. Zvolte **Uložit**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
