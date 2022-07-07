---
title: Vytvoření majetku
description: Tento článek popisuje, jak vytvořit majetek v modulu Správa majetku.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ab715be3bfdc380f5736fadd901af3ed78d7035
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016297"
---
# <a name="create-an-asset"></a>Vytvoření majetku

[!include [banner](../../includes/banner.md)]

 

Tento článek popisuje, jak vytvořit majetek v modulu Správa majetku.

1. Klikněte na **Správa majetku** > **Majetek** > **Všechen majetek** nebo **Aktivní majetek**.
2. Klikněte na tlačítko **Nový**.
3. V dialogovém okně **Vytvořit majetek** zadejte data týkající se **majetku** (ID majetku) a název majetku. V poli **Platnost** vyberte datum a čas majetku. Od tohoto data můžete majetek nainstalovat do funkčního umístění a také přesunout a nahradit majetek ve struktuře majetku.
4. V poli **typ** majetku vyberte typ majetku pro majetek (povinné pole). V případě potřeby vyberte **výrobce majetku** a **model majetku**. Pokud byl nastaven pouze jeden produkt, je tento produkt automaticky vybrán v poli **výrobce majetku**. Výběry dostupné v polích **Výrobce majetku** a **Model majetku** závisí na nastavení v poli [Výrobci a modely majetku](../setup-for-objects/product-and-model.md).
5. Ve skupině **Nadřazený majetek** je pole **Majetek** ve výchozím nastavení prázdné. V případě potřeby můžete vybrat nadřazený majetek a potom budou automaticky vyplněna všechna pole ve skupině **nadřazený majetek**.
    >[!NOTE]  
    >Když vyberete nadřazený majetek, jsou k dispozici dvě nebo tři karty: karta **Můj majetek** obsahuje majetek související s funkčními místy, do kterých můžete být přidělení (pracovník údržby, který je přihlášen k systému). Nejsou-li u pracovníka údržby ve formuláři [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md) nastavena žádná funkční umístění, nebude karta **Můj majetek** viditelná. Karta **Aktivní majetek** obsahuje seznam všech datových zdrojů, které jsou aktivní pro stav životnosti majetku. Karta **Zobrazení majetku** zobrazuje stromové zobrazení funkčních míst a datových zdrojů nainstalovaných v těchto umístěních.

6. Výchozí funkční umístění, které jste nastavili, je navrženo pro majetek v poli **Skupina majetku** > **Funkční místo**. V případě potřeby vyberte jiné funkční místo.

    >[!NOTE]
    >Po vytvoření můžete majetek nainstalovat do jiného funkčního umístění, pokud je to vyžadováno. Do funkčního umístění lze nainstalovat pouze majetek nejvyšší úrovně (majetek bez aktuálního nadřazeného majetku). To znamená, že jste nainstalovali nejvyšší úroveň a také veškerý podřízený majetek ve vybraném funkčním místě. Přečtěte si další informace o instalaci majetku do funkčních míst v poli [Úvod do funkčních míst](../functional-locations/introduction-to-functional-locations.md).

7. Klikněte na tlačítko **OK**.
8. Vyberte majetek v seznamu **Všechen majetek** a kliknutím na tlačítko **Upravit** přidejte k majetku další informace.

## <a name="general-information"></a>Obecné informace

Funkční místo, ke kterému se majetek vztahuje, se zobrazí v poli **funkční místo**. Pokud je majetek nadřazeným majetkem, zobrazí se počet podřízených položek majetku v poli **Děti**. Pokud je majetek podřízeným majetkem existujícího majetku, zobrazí se ID nadřazeného majetku v poli **Rodiče**.

Můžete upravit informace o **výrobci majetku** a **modelu majetku**, který se používá ke správě náhradních dílů, alternativních náhradních dílů a výchozích hodnot typu práce. Další informace naleznete v tématu [Výrobci a modely majetku](../setup-for-objects/product-and-model.md). V případě potřeby můžete také přidat další informace o **roce modelu** a **sériovém čísle**.

**Aktuální stav životního cyklu** se používají k definování, zda je majetek aktivní nebo neaktivní. Při vytváření majetku je tato fáze vždy nastavena na první fázi ve skupině fází majetku. Jakmile jste připraveni k aktivaci majetku, klikněte na možnost **aktualizovat stav majetku** a vyberte stav životního cyklu, který jste definovali jako aktivní, a klikněte na tlačítko **OK**.

**Poznámka:** Pokud je majetek nastaven na "neaktivní", není již možné pro tento majetek vytvořit pracovní příkazy. Nelze navíc naplánovat úlohy preventivní údržby pro neaktivní majetek.

Pole **Úroveň služby** a **Závažnost** se vztahují k pracovním příkazům vytvořeným pro majetek. Pole zobrazují hodnoty **úroveň služby** a **Závažnost** vypočítaná pro aktuální nastavení majetku. Informace o nastavení těchto hodnot získáte v části [Úrovně služeb majetku](../setup-for-objects/object-priorities.md) a [Typy kritičnosti majetku](../setup-for-objects/object-criticalities.md).

## <a name="asset"></a>Majetek

Pro majetek můžete vybrat **zdroj**. Výběr zdroje určuje, který kalendář se použije pro plánování pracovního příkazu. Výběr zdrojů se často používá pro dlouhodobý majetek. Zdroje a skupiny zdrojů jsou nastavené v části **Správa organizace** > **Zdroje** > **Skupiny zdrojů** nebo **Zdroje**.

V poli **číslo dlouhodobého majetku** můžete vybrat dlouhodobý majetek, který chcete s majetkem spojit. To platí, pokud váš majetek souvisí s investičním projektem.

- Pokud majetek souvisí s dlouhodobým majetkem, můžete vytvořit typ pracovního příkazu, který se použije pro pracovní příkazy spojené s investičním projektem. 
- Informace o dlouhodobém majetku pro majetek se vztahují k modulu **Dlouhodobý majetek** v aplikaci Dynamics 365 Supply Chain Management. To znamená, že v okně **Dlouhodobý majetek** > **Dlouhodobý majetek** > **Dlouhodobý majetek** můžete získat přehled projektů správy majetku, které mohou souviset s dlouhodobým majetkem, výběrem majetku v seznamu a zobrazením obsahu v podokně **Související informace** > **Související projekty**.


## <a name="details"></a>Podrobnosti

V poli **Aktivní od** se zobrazuje datum, ke kterému jste aktualizovali stav životního cyklu majetku na aktivní (viz [Stavy životního cyklu majetku](../setup-for-objects/object-stages.md) ohledně nastavení stavů životního cyklu majetku). Pokud již majetek není aktivní a vy jste aktualizovali stav životního cyklu majetku na neaktivní, je v poli **aktivní do** zobrazeno datum, od kterého je majetek neaktivní. V případě potřeby lze tato data ručně změnit.

V případě potřeby můžete do pole **Datum nahrazení** zadat očekávané datum pro náhradu majetku. Odhadovaná hodnota pro nahrazení majetku může být zadána do pole **Náhradní hodnota**. Příklad: informace o nahrazení můžete použít k porovnání s náklady na údržbu majetku a následně rozhodnout o koupi nového majetku, pokud náklady na údržbu stávajícího majetku rychle vzrostou.

## <a name="notes"></a>Poznámky

Na pevné záložce **Poznámky** můžete přidat poznámky týkající se majetku. Chcete-li do poznámky přidat informace o uživateli a datum/časové razítko, klepněte před napsání poznámky na tlačítko **Přidat časové razítko**.

## <a name="attributes"></a>Atributy

Na této pevné záložce můžete nastavit hodnoty pro atributy majetku. Tyto atributy lze použít k popisu vlastností vztahujících se k danému majetku, například velikosti, hmotnosti nebo konfigurace počítače.

Klikněte na **Přidat řádek** a vyberte typ atributu. Dále vložte **hodnotu** vztahující se k typu atributu a uložte záznam.

>[!NOTE] 
>Můžete získat přehled typů atributů majetku a jejich vztah k majetku v polích **atribut majetku** a **přehled atributů majetku**. Další informace viz [Přehled atributů majetku](../objects/object-specification-overview.md).

## <a name="vendor"></a>Dodavatel

Na pevné záložce **Dodavatel** vyberte účet dodavatele pro majetek. Pokud byla poskytnuta záruka na dodavatele, můžete zde vložit informace o záruce.

## <a name="address"></a>Adresa

Na pevné záložce **Adresa** můžete zadat adresu zařízení. Pokud není u majetku zadaná žádná adresa, majetek použije adresu nadřazeného majetku, jestliže má adresu. Pokud žádná adresa není spojena s majetkem nebo nadřazeným majetkem v hierarchii majetku, může být použita adresa funkčního umístění, ve kterém je majetek instalován. Pokud toto funkční umístění nemá související adresu, použije se pro majetek adresa nadřazeného funkčního umístění.

## <a name="asset-management-plans"></a>Plány údržby majetku

Plány údržby se používají pro plánování úloh preventivní údržby v pravidelných intervalech u majetku. Na této pevné záložce můžete nastavit řádky plánu údržby pro vybraný majetek. Pro různé majetky lze nastavit kola údržby, na kterých je třeba v pravidelných intervalech provádět podobné úkoly. Na kartě **Plány údržby funkčního místa** se zobrazí plány údržby související s funkčním místem, ve kterém je majetek instalován.

>[!NOTE]
>Pokud odstraníte řádek plánu údržby nebo kolo údržby spojené s majetkem v části **Všechen majetek**, automaticky odstraníte také všechny plány údržby se stavem Vytvořeno, které byly vytvořeny na základě plánu údržby nebo kola údržby.

## <a name="functional-location-maintenance-plans"></a>Plány údržby funkčního místa

Na této pevné záložce získáte přehled plánů údržby souvisejících s funkčním místem, na kterém je majetek instalovaný.

## <a name="maintenance-rounds"></a>Pořadí údržby

Na této pevné záložce můžete přidat nebo odebrat kola údržby, která jsou spojena s majetkem.

## <a name="financial-dimensions"></a>Finanční dimenze

Můžete vybrat finanční dimenze pro majetek.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]