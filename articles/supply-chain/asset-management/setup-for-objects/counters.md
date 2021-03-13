---
title: Měrný systém majetku
description: Toto téma vysvětluje, jak vytvořit typy měrného systému majetku v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 37f47b3d9ba0344b96db5626359e2a99a1a40f9c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018514"
---
# <a name="counters"></a>Čítače

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit typy čítačů v modulu Správa majetku. Typy čítačů majetku se používají k provádění registrací čítačů u majetku, například pokud jde o počet hodin výroby nebo množství vyrobeného majetku. Typy majetku souvisí s typy čítačů. To znamená, že čítačů majetku lze použít u majetku použít pouze v případě, že je u typu majetku použitého pro daný majetek nastaven čítač majetku.

Před provedením registrací čítače u majetku nejprve vytvořte typy čítače majetku, které chcete použít, v části **Čítače**. Dále můžete vytvořit registrace čítače u majetku v okně **Čítače**. 

Čítače je možné používat v plánech údržby. Řádek Plán údržby může být typu Čítač, například v souvislosti s počtem hodin výroby nebo vyrobeného množství. 

Registraci čítače majetku lze aktualizovat ručně nebo automaticky na základě hodin výroby nebo vyrobeného množství. Čítač lze nastavit pro použití jedné ze tří metod aktualizace (vybraných v poli **Aktualizovat** v **čítačích**):
  
- Ručně - hodnoty čítače je nutné registrovat ručně.  
- Výrobní hodiny - čítač je automaticky aktualizován na základě počtu výrobních hodin.  
- Množství výroby - čítač je automaticky aktualizován na základě počtu vyrobeného množství.  

>[!NOTE]
>Pokud se použije vyrobené množství, *všechny* registrované položky jsou zahrnuty do registrace čítače, dobrého množství i chybového množství. V případě potřeby je vždy možné provést ruční registraci čítače.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Vytvoření typů čítačů pro registrace čítačů majetku

1. Vyberte **Správa majetku** > **Nastavení** > **Typy majetku** > **Čítače**.
2. Zvolte **Nový** pro vytvoření nového typu čítače.
3. Zadejte ID do pole **Čítač** a název čítače do pole **Název**.
4. Na pevné záložce **Obecné** vyberte čítač v poli **Jednotka**.
5. V poli **Aktualizovat** vyberte metodu aktualizace, která bude použita pro čítač.
6. Vyberte Ano u přepínacího tlačítka **Zdědit hodnoty čítače**, pokud má podřízený majetek ve struktuře majetku automaticky zdědit registrace čítače provedené v nadřízeném majetku.
7. V poli **Agregovaný součet** vyberte metodu sumarizace, která má být použita pro čítač s použitím tohoto typu čítače. "Součet" je standardní výběr použitý pro nepřetržité přidávání registrovaných hodnot k celkové hodnotě. "Průměr" lze použít, pokud je čítač nastaven na sledování prahové hodnoty, například ohledně teploty, vibrací nebo opotřebení majetku. 
8. Do pole **Odchylka nad** zadejte horní úroveň v procentech pro ověření, zda jsou položky ručního čítače v očekávaném rozsahu. Ověření je založeno na lineárním nárůstu ve stávajících registracích čítače.
9. Do pole **Odchylka pod** zadejte dolní úroveň v procentech pro ověření, zda jsou položky ručního čítače v očekávaném rozsahu. Ověření je založeno na lineárním snížení ve stávajících registracích čítače.
10. V poli **Typ** vyberte typ zprávy (informace, upozornění, chyba), která se zobrazí, pokud se při provádění ručních registrací čítače vyskytnou odchylky mimo definovaný rozsah.
11. Na pevné záložce **Typy majetku** přidejte typy majetku, které by měly být schopny používat čítač.
12. Na pevné záložce **Související čítače majetku** přidejte čítač, který chcete automaticky aktualizovat při aktualizaci tohoto čítače.


>[!NOTE]
>Související čítač je automaticky aktualizován pouze v případě, že má odpovídající čítač typ majetku, ke kterému se vztahuje, v nastavení měrného systému majetku. Například: nastavíte čítač na "výrobní hodiny" a přidáte typ majetku " Motor nákladního automobilu". Při aktualizaci tohoto čítače je aktualizován také související čítač "benzín" se stejnými hodnotami čítače. Nastavení v poli **čítače** zahrnuje nastavení v poli "hodiny". U čítače "Benzín" by měl být na pevnou záložku **Typy majetku** přidán typ majetku Motor nákladního automobilu pro zajištění vztahu čítače. Na následujících snímcích obrazovky je uveden příklad nastavení v čítačích Hodiny a Benzín.

Když jsou typy majetku přidány k typu čítače v poli **Čítače**, je tento čítač automaticky přidán k typům majetku na pevné záložce v okně **čítače** v poli [Typy majetku](../setup-for-objects/object-types.md).

![Obrázek č. 1](media/071-setup-for-objects.png)

