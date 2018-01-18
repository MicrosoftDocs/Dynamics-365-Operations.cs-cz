---
title: "Nastavit upozornění na podvod"
description: "Toto téma vysvětluje, jak nastavit pravidla výstrahy pro zástupce z oddělení služeb zákazníkům zaměřené na potenciálně podvodné informace při zpracování objednávek. Můžete definovat zvláštní kódy, které jsou automaticky nebo ručně použity k blokování podezřelých objednávek."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans, SysOperationTemplateForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f57cdb44d5ed3b078478cf47b74d1a79ba10323c
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fraud-alerts"></a>Nastavení výstrah u podvodů

[!include[banner](includes/banner.md)]

Toto téma vysvětluje, jak lze nastavit kritéria a pravidla pro blokování potenciálně podvodných prodejních objednávek do doby, než je zkontrolujete. Funkce kontroly podvodu se používá při ověřování platnosti informací na prodejní objednávce. Pokud se informace v prodejní objednávce zdají být pochybné na základě kritérií a pravidel organizace týkajících se podvodu, objednávku lze pozdržet pro další kontrolu správcem.

> [!NOTE]
> Tuto funkci lze použít pouze se zpracováním prodejních objednávek pro kanál Retail Call Center. 

Pokud definujete kanálu kontaktního střediska, možnost **Povolit dokončení objednávky** musí být nastavena na **Ano**. Když je povoleno dokončení objednávky, uživatelé mohou zobrazit shrnutí objednávky a kliknout na tlačítko **Odeslat** pro dokončení objednávky. Uživatelům bude také poskytnuta možnost ručně pozdržet prodejní objednávku z důvodu nutné kontroly. Prodejní objednávky zadané uživatelem kontaktního střediska jsou zpracovávány prostřednictvím kontrolních pravidel a kritérií proti podvodu během procesu odeslání.

Existují dva typy kritérií podvodu, které systém systém použije ke kontrole, zda má být objednávka pozdržena kvůli kontrole:

-   **Statická pravidla** používají určitou hodnotu, například telefonní číslo, které je zakázané, nebo e-mailovou adresu, která byla označena proto, že byla v minulosti použita pro podvodné transakce. Na stránce **Statická podvodná data** lze informace o podvodu přidat ručně nebo pomocí importu dat, s výsledky připojenými k podvodné informaci. Pokud je zapnuta kontrola podvodu, každá zadaná prodejní objednávka bude porovnána se statickými daty. Pokud se data nacházejí buď ve fakturaci odběratele nebo dodací adrese, nebo pokud jsou data nalezena v dodací adrese na řádku prodeje, skóre všech jedinečných hodnot se sečte.  
-   **Dynamická pravidla** se skládají z proměnných a podmínek definovaných pro tyto proměnné. Pomocí dynamických pravidel lze zkontrolovat jiná kritéria, která nejsou definována ve statických pravidlech. Lze použít složitější výrazy AND/OR pro zvážení mnohých podmínek při určení, zda existuje pozitivní shoda proti kritériím pravidel a odesílané prodejní objednávce. Například, pokud uživatel chce pozdržet kvůli kontrole proti podvodu všechny objednávky odběratelů, které jsou vázány na hodnotu skupiny specifického a které objednávají konkrétní produkt, podmínky k ověření odběratele a produktu se definují na stránce **Pravidla** pomocí podmínky AND. Objednávka by spadala do pozdržení kvůli podvodu pouze tehdy, pokud by obě podmínky byly pravdivé a pokud by hodnota skóre přiřazená k pravidlu zvýšila celkové skóre podvodu nad minimální skóre podvodu stanovené v parametrech kontaktního střediska.

Uživatel kontaktního střediska může také ručně přidat objednávku do fronty pozdržení kvůli podvodu. Pokud je uživatel zadávající objednávku toho názoru, že objednávka odběratele může být podezřelá, a požaduje po jiném uživateli, aby dále zkontroloval platnost objednávky před jejím zpracováním, uživatel při zadávání objednávky může zvolit možnost **Ruční blokování kvůli podvodu** z rozevírací nabídky **Blokování** na stránce **Souhrn prodejní objednávky** (zobrazí se po zavolání funkce objednávky **Dokončit**). Uživatel bude vyzván k zadání poznámky a vysvětlení, proč se domnívá, že objednávka může být podvodná, aby měl další kontrolor více kontextu.

Všechny objednávky pozdržené prostřednictvím ručního blokování kvůli podvodu nebo systematickým výpočtem podvodného skóre se zobrazí na stránce **Blokování objednávky**, kde lze objednávky zkontrolovat a poté buď zrušit nebo uvolnit pro zpracování.

> [!NOTE]
> Použití více pravidel nebo výrazně složitých pravidel způsobí špatný výkonu systému při odesílání prodejních objednávek. Funkce upozornění na podvod nebyla optimalizována pro zpracování velkého objemu statických datových položek týkajících se podvodu a mnoha aktivních pravidel. Je třeba mít na paměti, že každé pravidlo se vyhodnocuje během funkce odesílání položky prodejní objednávky kontaktního střediska. Pravidla jsou vyhodnocována proti záhlaví prodejní objednávky a všem řádkům objednávky. Čím více existuje pravidel a čím více složitější jsou výrazy pravidel, tím déle bude trvat zpracování. Pokud máte velký počet položek řádku na objednávce a velký počet aktivních pravidel a položek statických dat, tento systematický proces přezkoumání a ověření všech dat a výpočtu skóre podvodu může mít dopad na výkon.  Organizace používající tuto funkci by měly vždy otestovat a potvrdit, že doba zpracování odeslání objednávky je přijatelná, dříve než použijí změny pravidel nebo statických kritérií podvodu v produkčním prostředí.

