---
title: Vytvoření možností pokrytí
description: Možnosti pokrytí v Microsoft Dynamics 365 Human Resources představují úrovně pokrytí volby účastníka v plánu nebo programu zaměstnanecké výhody.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 021fea7604af2fff833ddc6868d55a316ef70aae
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230170"
---
# <a name="create-coverage-options"></a>Vytvoření možností pokrytí

Možnosti pokrytí v Microsoft Dynamics 365 Human Resources představují úrovně pokrytí volby účastníka v plánu nebo programu zaměstnanecké výhody. Možnosti pokrytí mohou například zahrnovat **pouze zaměstnance** pro lékařský plán nebo **2x plat** pro plán životního pojištění. Po definování můžete znovu použít možnosti pokrytí zaměstnaneckých výhod. Můžete přidružit možnost k jednomu nebo více plánům.

Po definování možností pokrytí připojte možnosti pokrytí k typu plánu zaměstnaneckých výhod. Typ plánu je poté přidružen k plánu zaměstnaneckých výhod nebo k programu. Možnosti disponibility, které jsou přidruženy k typu plánu, jsou dostupné pro všechny plány vytvořené s tímto typem plánu. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** **Možnosti pokrytí**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | **Možnost pokrytí** | Jedinečný název možnosti pokrytí. |
   | **Popis** | Popis možnosti pokrytí. |
   | **Kód pokrytí** | Kódy pokrytí přiřazují minimální a maximální částky každému typu osoby s nárokem na pokrytí. Kód pokrytí indikuje, kdo má pokrytí nebo jaká částka pokrytí je povolena pro daný typ plánu. Částku pokrytí lze vyjádřit jako částku v korunách nebo v procentech. Například:</br></br>- **Emp+1** – aby měl zaměstnanec nárok, musí mít vybranou jednu závislou osobu (pokud jich je vybráno více, nárok se ztrácí).</br></br>- **Emp+family** – abyste mohl mít zaměstnanec nárok, musí mít vybrané nejméně dvě závislé osoby. |
   | **Maximální počet** | Maximální počet závislých osob |
   | **Stav** | Stav možnosti pokrytí. Je-li stav možnosti pokrytí nastaven na hodnotu Neaktivní, nelze pro typy plánů vybrat možnost Pokrytí. |
   | **Procento** | Procentuální částka. Toto pole je aktivní pouze v případě, že v poli kód disponibility byla vybrána možnost % x mzdy. |
   | **Dělitel** | Dělitel, který má být použit ve výpočtu po výběru kódu pokrytí % x platu. |
   | **Minimální procento** | Minimální procento, když vyberete kód procentuálního pokrytí. |
   | **Maximální procento** | Maximální procento, když vyberete kód procentuálního pokrytí. |

4. Ve skupinovém rámečku **Možnosti nároku na osobní kontakt** připojte ke každé možnosti nároku odpovídající osobní kontakty.

5. V části **Samoobsluha** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Povolit částku příspěvku zaměstnance** | Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku příspěvku na samoobslužné služby. Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky příspěvku, kterou zaměstnanec zadá do samoobsluhy zaměstnaneckých výhod. |
   | **Povolit částku pokrytí zaměstnance** | Určuje, zda mají mít zaměstnanci při výběru zaměstnaneckých výhod v případě zaměstnaneckých výhod možnost upravovat částku pokrytí na samoobslužné služby. Pokud zaškrtnete toto políčko, systém vypočítá parametry plánu zaměstnaneckých výhod na základě částky pokrytí, kterou zaměstnanec zadá do samoobsluhy zaměstnance. |

6. Zvolte **Uložit**. 
