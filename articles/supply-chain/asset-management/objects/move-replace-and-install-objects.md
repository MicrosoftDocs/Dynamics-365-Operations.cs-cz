---
title: Přesun, nahrazení a instalace majetku
description: Toto téma vysvětluje, jak přesunout, nahradit a nainstalovat majetek v modulu Správa majetku.
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
ms.openlocfilehash: c0e6306698d351d33cae627e3741ad9a2eb6d893
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783137"
---
# <a name="move-replace-and-install-assets"></a>Přesun, nahrazení a instalace majetku

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Toto téma vysvětluje, jak přesunout, nahradit a nainstalovat majetek v modulu Správa majetku. Můžete vytvořit jednotlivý majetek, který nemá žádné vztahy k jiným majetkům, nebo můžete vytvořit strukturu majetku, která zahrnuje nadřazený majetek (majetek nejvyšší úrovně) a související podřízený majetek (dílčí majetek). V modulu Správa majetku existují tři přístupy k přesunu a změně umístění majetku:

- **Přesunout** – Přesun majetku buď do jiné struktury majetku nebo do jiného umístění ve stejné struktuře majetku.
- **Nahradit** – Dočasně odstraňte majetek ze struktury majetku, aby mohl být opraven nebo obnoven, a poté znovu přidejte obnovený majetek zpět do struktury majetku později. Můžete také trvale nahradit použitý majetek novým majetkem.
- **Instalovat** – Instalace nadřazeného majetku a souvisejícího podřízeného majetku na funkční místo.

> [!NOTE]
> Majetek, který přesunete, nahradíte nebo nainstalujete, může souviset s jiným funkčním místem. V takovém případě může majetek využívat finanční dimenze funkčního místa. Na stránce **Typy funkčních míst** nastavte zpracování finančních dimenzí na funkčních místech.

## <a name="move-asset"></a>Přesun majetku

Použijte funkci **Přesunout majetek** – pro přesun majetku buď do jiné struktury majetku nebo do jiného umístění ve stejné struktuře majetku. Majetek můžete také přesunout mimo strukturu majetku tak, aby se stal samostatným majetkem, který nemá žádné vztahy se strukturou.

> [!NOTE]
> Tuto funkci nepoužívejte, pokud je majetek opraven nebo dočasně nahrazen. Místo toho použijte funkci **Nahradit majetek**, která je popsána dále v tomto tématu.

1. Zvolte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek** nebo **Aktivní majetek**.
2. V seznamu vyberte majetek, který chcete přesunout. Pokud má majetek podřízený majetek, přesunete také tento majetek.
3. Zvolte **Přesunout majetek**.
4. Chcete-li majetek přesunout tak, aby se stal součástí struktury majetku, vyberte nový nadřazený majetek v poli **Nadřazený majetek**. Pokud přesouváte podřízený majetek a chcete jej nastavit jako samostatný majetek, který nemá žádné vztahy ke struktuře, ponechejte pole **Nadřazený majetek** prázdné.
5. Ve výchozím nastavení je pole **Začátek platnosti** automaticky nastaveno na aktuální datum a čas. Můžete však vybrat jiné datum a čas, od kterého je přesun majetku platný.
6. Vyberte **OK**.

## <a name="replace-asset"></a>Nahrazení majetku

Použijte funkci **Nahradit majetek** v souvislosti s opravami, obnovou nebo trvalým nahrazením opotřebeného majetku novým majetkem. Tato funkce se používá k nahrazení podřízeného majetku ve struktuře majetku. Pro nadřazený majetek (to znamená majetek, který momentálně nemá nadřazený majetek) se tato náhrada provádí na funkčním místě. Další informace o tom, jak nahradit nadřazený majetek na funkčním místě, naleznete v tématu [Instalace majetku na funkčních místech](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Pokud dílna souvisí s výrobním oddělením, můžete vytvořit funkční místa, jako **Oprava**, **Odpad** a **Sklad** pro zpracování oprav a nahrazení majetku.

1. Zvolte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek** nebo **Aktivní majetek**.
2. V seznamu vyberte podřízený majetek, který chcete nahradit. Pokud má majetek podřízený majetek, nahradíte také tento majetek.
3. Vyberte **Nahradit majetek**.

    Pole **Změna struktury** zobrazuje poslední datum a čas, kdy byl vybraný majetek a související podřízený majetek přesunut ve struktuře majetku.

4. V části **Vybraný majetek** vyberte v poli **Cílové funkční místo** funkční umístění, do kterého chcete majetek přesunout. Vyberte například místo **Oprava** nebo **Odpad**.

    V části **Nadřazený majetek** zobrazí pole **Začátek platnosti** datum a čas, kdy byl nadřazený majetek a související podřízený majetek instalován nebo přesunut na aktuální funkční místo.

5. V části **Nový majetek** v poli **Majetek** vyberte majetek, který chcete vložit jako dočasnou nebo trvalou náhradu vybraného majetku. Tento majetek může být aktuálně umístěn na jiné funkční místo, jako například **Sklad**.
7. V části **Platnost od** je pole **Začátek platnosti** automaticky nastaveno na aktuální datum a čas ve výchozím nastavení. Můžete však vybrat jiné datum a čas, od kterého je nahrazení majetku platné.
8. Vyberte **OK**.

## <a name="install-asset"></a>Instalace majetku

K instalaci struktury majetku do funkčního místa použijte funkci **Nainstalovat majetek**.

> [!NOTE]
> Vždy vyberte nadřazený majetek. Nadřazený majetek a související podřízený majetek budou přesunuty do vybraného funkčního místa.

1. Zvolte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek** nebo **Aktivní majetek**.
2. V seznamu vyberte nadřazený majetek, který chcete nainstalovat do jiného funkčního místa.
3. Vyberte **Instalovat majetek**.

    Část **Atributy** zobrazuje atributy majetku, které jsou nastaveny u nadřazeného majetku.

4. V poli **Funkční místo** zvolte nové místo.
5. Ve výchozím nastavení je pole **Začátek platnosti** automaticky nastaveno na aktuální datum a čas. Můžete však vybrat jiné datum a čas, od kterého je instalace ve struktuře majetku platná.
6. Vyberte **OK**.
