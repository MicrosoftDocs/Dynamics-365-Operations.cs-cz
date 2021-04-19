---
title: Úvod do majetku
description: Toto téma obsahuje přehled majetku v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91c4ad4a96ce94c911066604794420c335a491b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808561"
---
# <a name="introduction-to-assets"></a>Úvod do majetku

[!include [banner](../../includes/banner.md)]

 

Toto téma obsahuje přehled majetku v modulu Správa majetku. *Majetek* je jakýkoliv typ zařízení, například stroj nebo část stroje vyžadující údržbu, servis nebo opravu.

Majetek je automaticky aktualizován o související informace. Tyto informace mohou například souviset s novými nebo aktualizovanými pracovními příkazy. Majetek můžete vytvořit buď pomocí položky nabídky **Všechen majetek** nebo položky nabídky **Čekající majetek**. Toto téma vysvětluje, jak vytvořit majetek pomocí položky nabídky **Všechen majetek**. Informace o způsobu vytvoření majetku pomocí položky nabídky **Čekající majetek** naleznete v tématu [Vytvoření majetku na základě nákupních objednávek](../objects/create-objects-based-on-purchase-orders.md).

## <a name="all-assets"></a>Všechen majetek

Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Všechen majetek**. Na stránce se seznamem **Všechen majetek** je zobrazen veškerý majetek a některé informace, které s nimi souvisejí. Chcete-li zobrazit pouze aktivní majetek, vyberte **Aktivní majetek**. Chcete-li zobrazit pouze majetek, který je nainstalován na funkčních místech, se kterými jste spojeni jako pracovník údržby, vyberte **Můj aktivní majetek**. (Tento vztah je nastaven na stránce **Pracovníci**. Další informace naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).)

V zobrazení mřížky **Všechen majetek** vyberte odkaz ve sloupci **Majetek**, chcete-li zobrazit podrobnosti o vybraném záznamu. Chcete-li záznam upravit, klikněte na tlačítko **Upravit**. V zobrazení podrobností jsou uvedeny podrobné informace vztahující se k danému majetku. Podokno **Související informace** vpravo obsahuje další informace související s majetkem. Rozbalením podokna zobrazíte související informace o vybraném majetku.

Tlačítka v podokně akcí jsou uspořádána na kartách. Následující tabulka stručně popisuje tlačítka, která souvisejí se správou majetku.

| Název tlačítka          | Popis                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Úpravy                 | Upravte vybraný majetek.                                                                                                                                         |
| Nové                  | Vytvořte nový majetek.                                                                                                                                                |
| Odstranit               | Odstraňte vybraný majetek.                                                                                                                                       |
| Přesun majetku           | Přesuňte majetek buď do jiné struktury majetku nebo do jiného umístění ve stejné struktuře majetku.                                                                                         |
| Náhrada majetku        | Nahraďte jeden podřízený majetek v hierarchii majetku jiným majetkem.                                                                                                  |
| Instalace majetku        | Instalujte majetek na funkční místo.                                                                                                                          |
| Kopírovat majetek           | Kopírujte hierarchii majetku do jiného majetku.                                                                                                                          |
| Požadavky             | Otevřete stránku se seznamem **Aktivní požadavky**, kde můžete zobrazit požadavky na údržbu, které byly pro vybraný majetek vytvořeny.                                                                         |
| Historie událostí        | Zobrazte přehled různých registrací, které byly provedeny u majetku.                                                                                                         |
| Kusovník majetku            | Zobrazte seznam všech položek (náhradních dílů a jiných položek), které se používají u majetku.                                                                                  |
| Pracovní příkazy          | Otevřete stránku **Aktivní pracovní příkazy**, kde můžete zobrazit pracovní příkazy pro majetek.                                                                                        |
| Kontrolní seznam            | Zobrazte přehled kontrolních seznamů údržby a měrných systémů, které byly zaregistrovány u majetku.                                                                                                 |
| Prostoj údržby | Vytvořte nebo zobrazte registrace prostoje údržby u majetku.                                                                                                       |
| Transakce projektu | Zobrazte všechny zaúčtované transakce, které souvisejí s pracovními příkazy, které byly pro majetek vytvořeny.                                                                                       |
| Měrné systémy majetku       | Vytvořte nebo zobrazte měrné systémy u majetku.                                                                                                               |
| Rozvrh údržby | Otevřete stránku se seznamem **Otevřít rozvrh údržby**, kde můžete zobrazit plány údržby, požadavky na údržbu a pořadí údržby, které jsou přidružené k majetku a mají stav **Vytvořeno**. |
| Aktualizace stavu majetku   | Aktualizujte stav životního cyklu majetku. Na stránce se seznamem **Všechen majetek** můžete vybrat více majetků a potom pro všechny najednou aktualizovat stav životního cyklu majetku.              |
| Protokol stavu životního cyklu  | Otevřete protokol, který zobrazuje stavy životního cyklu vybraného majetku.                                                                                                                 |
| Dokumenty majetku      | Zobrazte seznam dokumentů připojených k majetku. Tyto dokumenty se nastavují v **Správa majetku** \> **Nastavení** \> **Dokumenty majetku**.                 |
| Atributy           | Vytvořte nebo zobrazte atributy majetku.                                                                                                                             |
| Obrázek                | Vyberte obrázek pro majetek.                                                                                                                                   |
| Nadřazený majetek        | Zobrazte historii nadřazeného majetku pro vybraný majetek.                                                                                                                |
| Funkční místa | Zobrazte historii funkčního místa pro vybraný majetek.                                                                                                          |
| Vyhodnocení stavu | Zaregistrujte měření vyhodnocení stavu majetku.                                                                                                         |
| Závady               | Otevřete stránku se seznamem **Závada majetku**, kde můžete zobrazit poruchy, které byly registrovány u majetku.                                                                                             |
| Řízení nákladů         | Porovnejte rozpočtové náklady a skutečné náklady na majetku.                                                                                                              |
| Řízení hodin         | Porovnejte hodiny prognózy a skutečné hodiny na majetku.                                                                                                              |
| Ukazatele KPI majetku           | Vypočítejte a zobrazte klíčové ukazatele výkonu (KPI) pro majetek.                                                                                              |
| Typ úloh            | Zobrazte přehled aktuálních výchozích typů úloh pro majetek.                                                                                                            |
| Typy kritických záležitostí    | Zobrazte nebo aktualizujte typy kritických záležitostí majetku.                                                                                                                              |
| Náhradní díly          | Zobrazte seznam schválených a alternativních náhradních dílů, které lze na majetku použít.                                                                               |
| Spotřeba majetku    | Vytiskněte sestavu zobrazující registrace spotřeby u majetku                                                                                                |
| Závada majetku          | Vytiskněte sestavu zobrazující registrace závad u majetku                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]