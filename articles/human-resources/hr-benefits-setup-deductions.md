---
title: Konfigurace srážek
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008376"
---
# <a name="configure-deductions"></a>Konfigurace srážek

[!include [banner](includes/preview-feature.md)]

Srážky v Microsoft Dynamics 365 Human Resources slouží k určení toho, jak často má být provedena srážka z výplaty zaměstnance u každé výhody. Srážky jsou efektivní podle data, takže je možné uchovat historický záznam informací o srážce. 

1. V pracovním prostoru **Správa výhod** vyberte v části **Nastavení** možnost **Srážky**.

2. Zvolte **Nové**.

3. Zadejte hodnoty pro zbývající pole:

   | Pole | Popis |
   | --- | --- |
   | Odpočet | Jedinečné ID, které se používá k identifikaci srážky ze zaměstnaneckých výhod. |
   | Popis | Popis srážky. |
   | Účinné: | Počáteční datum. Výchozí hodnotou je aktuální systémové datum. |
   | Vypršení platnosti | Koncové datum. Výchozí hodnota je 12/31/2154, což znamená nikdy. |
   | Záhlaví | Kód záhlaví ze systému mezd, který bude použit pro část srážky pro zaměstnance při zpracování zaměstnaneckých výhod. Používá se v případě, že používáte poskytovatele mezd od třetí strany. |
   | Odkaz srážky ze mzdy zaměstnance | Kód srážky z mzdového systému, který tato srážka použije pro část zaměstnance srážky při zpracování zaměstnaneckých výhod do mzdy. |
   | Záhlaví částky | Kód záhlaví ze systému mezd, který bude použit pro část srážky pro zaměstnance při zpracování zaměstnaneckých výhod. Běžně se používá v případě, že používáte poskytovatele mezd od třetí strany. |
   | Lze odstranit | Určuje, zda může exportovaná hodnota z Dynamics 365 for Finance and Operations způsobit odstranění hodnoty v systému mezd. |
   | Spárované sloupce | Určuje, zda má být exportována částka záhlaví a srážky ve spárováných sousedících sloupcích do mzdového systému. |
   | Datum platnosti změny | Datum, kdy změna srážky zaměstnanecké výhody vstoupí v platnost. K tomuto datu systém automaticky změní srážku zaměstnanecké výhody a aktualizuje všechny plány zaměstnaneckých výhod spojené s touto srážkou, pokud spustíte zpracování aktualizace změny srážky. |
   | Změna srážek dokončena | Jakmile budou dokončeny změny srážky v procesu aktualizace změny srážky, bude automaticky zaškrtnuto políčko Změna srážky dokončena. |
   
4. Chcete-li sledovat a spravovat změny v nastavení sazby zaměstnaneckých výhod, vyberte **Akce** a potom vyberte **Spravovat verze**.

5. Zvolte **Uložit**. 
