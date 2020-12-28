---
title: Práce s předvolbami stylu
description: Toto téma popisuje, jak pracovat s předvolbami stylu pracoviště v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 250f2386cefee8bef45df66c4eef31b4e7fc2686
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410851"
---
# <a name="work-with-style-presets"></a>Práce s předvolbami stylu

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak pracovat s předvolbami stylu pracoviště v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Předvolba stylu je uložená sada všech hodnot stylu, které lze tvořit napříč motivem webu. Může být použit k okamžité změně vzhledu webu od tvůrce webu. Předvolby stylů umožňují tvůrcům obchodního webu rychle měnit, zobrazovat náhledy a aktivovat sadu hodnot stylů na svém webu, aniž by museli používat Cascading Style Sheets (CSS) nebo nasazovat motivy. Styly písem, styly tlačítek a barvy webu jsou typickými příklady proměnných stylů, které lze spravovat pomocí předvoleb stylů.

Sada proměnných stylů, které jsou k dispozici na webu, je určena knihovnou motivů a modulů, která je nasazena v klientovi webu. Online sada pro vývoj softwaru (SDK) Dynamics 365 Commerce umožňuje vývojářům implementovat tolik proměnných stylu s možnosti autorství, kolik vyžaduje dané téma. Povolením více proměnných stylu může vývojář motivu dát konečný výběr stylů stránek do rukou tvůrců webů. Proto mohou vývojáři aktualizovat a zobrazovat náhledy stylů webu pomocí sady nástrojů. Tato funkce je také užitečná pro všechny scénáře, kde přímé změny motivů nebo CSS způsobí zbytečnou zátěž.

Motivy, ve kterých jsou povoleny autorizovatelné proměnné stylu, vyžadují výchozí předvolbu stylu. Mohou volitelně zahrnovat další přednastavené možnosti jako součást nasazeného balíčku motivu. Například může být nasazen motiv, který má jednu výchozí předvolbu stylu „moderní světlá“. Alternativně může kromě výchozí předvolby zahrnovat další možnosti předvoleb stylu, například „moderní tmavý“, „archivní světlá“ nebo „archivní tmavá“. Tyto vestavěné předvolby motivů jsou vytvářeny vývojáři a mohou být použity jako výchozí body pro nové návrhy stránek.

Ve Tvůrci stránek si mohou autoři vybrat z předdefinovaných předvoleb motivů nebo si mohou pomocí aktivovaných proměnných stylu vytvořit vlastní předvolby stylu a přizpůsobení. Přednastavení stylu lze zobrazit v tvůrci stránek před jeho aktivací na živém webu. Po revizi změn autorova stylu lze přednastavení stylu pro aktivní web nastavit na „aktivní“.

## <a name="preview-a-style-preset"></a>Náhled předvolby stylu

Chcete-li zobrazit náhled předvolby stylu na vašem webu v nástroji pro tvorbu webu, postupujte takto.

1. V levém navigačním podokně vašeho webu přejděte na **Nastavení webu \> Návrh**.
1. Na kartě **Předvolby stylu** v horní části editoru návrhů v seznamu **Dostupné předvolby** vyberte předvolbu a poté vyberte **Zobrazit** pro přechod do editoru předvoleb.

    Pokud v současnosti neexistují žádné předvolby v seznamu **Dostupné předvolby**, získáte informace o tom, jak vytvořit vlastní předvolbu stylu, v tématu [Vytvoření vlastní předvolby stylu](#create-a-custom-style-preset).

    > [!NOTE]
    > Předvolby, které byly součástí motivu, jsou označeny a **integrovaným** odznakem. Tyto integrované předvolby jsou pouze pro čtení. Chcete-li zkopírovat integrovanou předvolbu jako novou přizpůsobitelnou předvolbu, vyberte tlačítko se třemi tečkami (**...**) pro předvolbu a poté vyberte **Uložit jako**.

1. Na příkazovém řádku vyberte možnost **Náhled**.
1. Vyberte ze svého webu adresu URL, kterou chcete použít k náhledu předvolby stylu, a poté vyberte **OK**.
1. Vyberte variantu adresy URL specifickou pro daný kanál a národní prostředí, kterou chcete zobrazit, výběrem názvu varianty. Otevře se nové okno prohlížeče náhledu, kde se vybraná předvolba stylu použije na zadanou stránku.

> [!NOTE]
> Adresa URL náhledu je trvalá a ověřená. Proto ji můžete zkopírovat, vložit a odeslat dalším ověřeným spolupracovníkům k posouzení, než ji na svém živém webu nastavíte jako „aktivní“. Adresa URL náhledu je také užitečná pro kontrolu stylů na různých zařízeních, v různých prohlížečích a na různých obrazovkách.

> [!TIP]
> Při úpravě předvolby stylu může být užitečné ponechat okno prohlížeče náhledu otevřené v samostatném okně prohlížeče, abyste mohli rychle ověřit své změny. Po uložení změn do předvolby obnovte otevřené okno prohlížeče náhledu a ověřte tak uživatelské prostředí.

## <a name="create-a-custom-style-preset"></a>Vytvoření vlastní předvolby stylu

Chcete-li vytvořit vlastní předvolbu stylu v nástroji pro tvorbu webu, postupujte následovně.

1. V levém navigačním podokně vašeho webu přejděte na **Nastavení webu \> Návrh**.
1. Na kartě **Předvolby stylu** v horní části editoru návrhů, na panelu příkazů, vyberte **Nová předvolba**.
1. Zadejte název a popis nové předvolby a vyberte **Uložit**. Je vytvořena nová přizpůsobitelná předvolba, která jako výchozí bod používá výchozí hodnoty motivu.

> [!NOTE]
> Můžete také vytvořit novou předvolbu vlastního stylu z kterékoli stávající předvolby výběrem tlačítka se třemi tečkami (**...**) pro tuto předvolbu a následným výběrem **Uložit jako**. Případně vyberte **Uložit jako** na příkazovém řádku v editoru předvoleb.

## <a name="modify-global-and-module-type-style-values"></a>Úprava globálních hodnoty a hodnot typu stylu modulu

Některé proměnné stylu motivu jsou sdíleny mezi více typy modulů. Tyto proměnné stylu jsou označovány jako *globální* proměnné stylu. Příklady zahrnují primární barvy webů, výchozí styly písem a styly tlačítek. Nastavením globálních proměnných můžete změnit vzhled mnoha různých typů modulů.

Některé hodnoty stylu mohou být jedinečné pro určitý typ modulu nebo mohou případně přepsat výchozí globální hodnotu. Pokud motiv webu implementoval proměnné stylu typu modulu, autoři tvůrce webu mohou přizpůsobit styl typu modulu nezávisle na globálním nastavení. Proměnné typu modulu mohou rozšířit nebo přepsat globální proměnné stylu v motivu.

> [!NOTE]
> Hierarchie hodnot stylů na webu se chová následujícím způsobem. Hodnoty stylů, které se zobrazují dále vpravo, přepíší hodnoty stylů vlevo od nich.
>
> Výchozí hodnoty motivu \< Globální hodnoty stylu \< Hodnoty stylu typu modulu \< přepis CSS

Chcete-li změnit globální hodnoty předvoleb stylu nebo typ modulu v nástroji pro tvorbu stránek, postupujte takto.

1. V levém navigačním podokně vašeho webu přejděte na **Nastavení webu \> Návrh**.
1. Na kartě **Předvolby stylu** v horní části editoru návrhů vyberte **Zobrazení** pro jakoukoli předvolbu stylu, abyste přešli do editoru předvoleb.
1. Vyberte **Náhled** a poté podle pokynů pro výběr adresy URL otevřete náhled předvolby v okně prohlížeče. Ponechte toto okno prohlížeče náhledu otevřené.
1. V editoru předvoleb vyberte **Upravit** v pravém horním rohu.
1. Pomocí ovládacích prvků proměnné stylu v editoru můžete změnit některé globální hodnoty stylu.
1. V horní části editoru na kartě **Moduly** napravo od **Globální** vyberte typ modulu, u něhož musí být vytvořen styl.
1. Pomocí ovládacích prvků stylu změňte některé hodnoty pro typ modulu.
1. Až budete připraveni zobrazit náhled změn, vyberte **Uložit** na příkazovém řádku.
1. Vraťte se do otevřeného okna prohlížeče náhledu a obnovte jej. Náhled v okně celého prohlížeče je užitečný pro kontrolu změn stylů v různých bodech přerušení zobrazení, v různých prohlížečích a na různých platformách zařízení.
1. Po dokončení a ověření všech změn vyberte **Dokončit úpravy** v pravém horním rohu editoru.

> [!NOTE]
> Pokud upravujete předvolbu stylu, která je na vašem webu aktuálně aktivní, uvidíte modrý odznak **Aktivní** v editoru. Tento symbol označuje, že předvolba je na vašem webu aktuálně aktivní. Pokud změníte aktivní předvolbu, vyberte **Publikovat**, aby se tyto změny přenesly na váš živý web.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Zajistěte, aby byla na vašem živém webu aktivní nový předvolba stylu

Chcete-li nastavit novou předvolbu stylu jako novou aktivní předvolbu na svém webu, postupujte následovně.

- Vyberte **Nastavit jako aktivní tlačítko** na jednom z těchto míst:

    - Příkazový řádek v editoru předvoleb stylu
    - Nabídka tlačítka se třemi tečkami (**...**) pro všechny dostupné předvolby v hlavním zobrazení na kartě **Předvolby stylu** v **Nastavení webu \>Design**

Hodnoty stylu předvolby se aktivují na vašem veřejně přístupném webu.

## <a name="additional-resources"></a>Další prostředky

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání uvítací zprávy](add-welcome-message.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)
