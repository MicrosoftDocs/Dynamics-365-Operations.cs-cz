---
title: Měrný systém majetku
description: Toto téma vysvětluje, jak vytvořit typy měrného systému majetku v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783133"
---
# <a name="asset-measures"></a>Mšrné systémy majetku

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Toto téma vysvětluje, jak vytvořit typy měrného systému majetku v modulu Správa majetku. Typy měrných systémů majetku se používají k provádění registrací měrného systému u majetku, například pokud jde o počet hodin výroby nebo množství vyrobeného majetku. Typy majetku souvisí s typy měrného systému majetku. To znamená, že měrný systém majetku lze použít u majetku použít pouze v případě, že je u typu majetku použitého pro daný majetek nastaven měrný systém majetku.

Před provedením registrací měrného systému u majetku nejprve vytvořte typy měrného systému majetku, které chcete použít, v části **Čítače**. Dále můžete vytvořit registrace měrného systému u majetku v okně **Měrný systém majetku**. 

Měrný systém majetku je možné používat v plánech údržby. Řádek Plán údržby může být typu Čítač, například v souvislosti s počtem hodin výroby nebo vyrobeného množství. 

Registraci měrného systému majetku lze aktualizovat ručně nebo automaticky na základě hodin výroby nebo vyrobeného množství. Měrný systém majetku lze nastavit pro použití jedné ze tří metod aktualizace (vybraných v poli **Aktualizovat** v **čítačích**):
  
- Ručně - hodnoty měrného systému majetku je nutné registrovat ručně.  
- Výrobní hodiny - čítač je automaticky aktualizován na základě počtu výrobních hodin.  
- Množství výroby - čítač je automaticky aktualizován na základě počtu vyrobeného množství.  

>[!NOTE]
>Pokud se použije vyrobené množství, *všechny* registrované položky jsou zahrnuty do registrace měrného systému, dobrého množství i chybového množství. V případě potřeby je vždy možné provést ruční registraci měrného systému majetku.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Vytvoření typů čítačů pro registrace čítačů majetku

1. Vyberte **Správa majetku** > **Nastavení** > **Typy majetku** > **Čítače**.
2. Zvolte **Nový** pro vytvoření nového typu měrného systému majetku.
3. Zadejte ID do pole **Čítač** a název čítače do pole **Název**.
4. Na pevné záložce **Obecné** vyberte měrnou jednotku v poli **Jednotka**.
5. V poli **Aktualizovat** vyberte metodu aktualizace, která bude použita pro měrný systém majetku.
6. Vyberte Ano u přepínacího tlačítka **Zdědit hodnoty čítače**, pokud má podřízený majetek ve struktuře majetku automaticky zdědit registrace měření majetku provedené v nadřízeném majetku.
7. V poli **Agregovaný součet** vyberte metodu sumarizace, která má být použita pro měrný systém majetku s použitím tohoto typu měrného systému majetku. "Součet" je standardní výběr použitý pro nepřetržité přidávání registrovaných hodnot k celkové hodnotě. "Průměr" lze použít, pokud je měrný systém majetku nastaven na sledování prahové hodnoty, například ohledně teploty, vibrací nebo opotřebení majetku. 
8. Do pole **Odchylka nad** zadejte horní úroveň v procentech pro ověření, zda jsou položky ručního měrného systému majetku v očekávaném rozsahu. Ověření je založeno na lineárním nárůstu ve stávajících registracích měrného systému majetku.
9. Do pole **Odchylka pod** zadejte dolní úroveň v procentech pro ověření, zda jsou položky ručního měrného systému majetku v očekávaném rozsahu. Ověření je založeno na lineárním snížení ve stávajících registracích měrného systému majetku.
10. V poli **Typ** vyberte typ zprávy (informace, upozornění, chyba), která se zobrazí, pokud se při provádění ručních registrací měrného systému majetku vyskytnou odchylky mimo definovaný rozsah.
11. Na pevné záložce **Typy majetku** přidejte typy majetku, které by měly být schopny používat měrný systém majetku.
12. Na pevné záložce **Související měrné jednotky majetku** přidejte měrné systémy majetku, který chcete automaticky aktualizovat při aktualizaci tohoto měrného systému majetku.


>[!NOTE]
>Související měrný systém majetku je automaticky aktualizován pouze v případě, že má odpovídající měrný systém majetku typ majetku, ke kterému se vztahuje, v nastavení měrného systému majetku. Například: nastavíte měrný systém majetku na "výrobní hodiny" a přidáte typ majetku " Motor nákladního automobilu". Při aktualizaci tohoto měrného systému majetku je aktualizován také související čítač "benzín" se stejnými hodnotami měrného systému majetku. Nastavení v poli **čítače** zahrnuje nastavení v poli "hodiny". U měrného systému majetku "Benzín" by měl být na pevnou záložku **Typy majetku** přidán typ majetku Motor nákladního automobilu pro zajištění vztahu měrného systému majetku. Na následujících snímcích obrazovky je uveden příklad nastavení v měrném systému Hodiny a Benzín.

Když jsou typy majetku přidány k typu měrného systému majetku v poli **Čítače**, je tento měrný systém majetku automaticky přidán k typům majetku na pevné záložce v okně **čítače** v poli [Typy majetku](../setup-for-objects/object-types.md).

![Obrázek č. 1](media/071-setup-for-objects.png)


