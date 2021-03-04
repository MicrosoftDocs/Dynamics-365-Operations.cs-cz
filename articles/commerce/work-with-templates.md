---
title: Práce se šablonami
description: Toto téma popisuje, jak pracovat s šablonami v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a3fc4259a76f6edcfaa0b8f6e08292477c6c0835
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410796"
---
# <a name="work-with-templates"></a>Práce se šablonami


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak pracovat s šablonami v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Jak bylo uvedeno v [Přehledu šablon a rozvržení](templates-layouts-overview.md), šablony definují sadu možností, které jsou k dispozici pro navazující autory. Šablony jsou užitečné pro tým pro vytváření webů v podniku z několika důvodů a dobře strukturované šablony vám mohou pomoci se všemi následujícími cíli:

- Zjednodušte prostředí pro každodenní role editora obsahu.

    - Možnosti modulu filtrování tak, aby byly v určité části stránky zobrazeny pouze relevantní moduly. (Část marketingové šablony lze například nakonfigurovat tak, aby odfiltroval nepodstatné moduly, které by v tomto kontextu neměly být nikdy použity, a které budou pouze zkomplikovat úlohy vytváření obsahu, pokud jsou zobrazeny.)
    - Nakonfigurujte výchozí nastavení modulu, aby se zlepšila efektivita vytváření.
    - Definujte výchozí fragmenty stránek, které pomáhají zlepšit efektivitu vytváření. (Například fragmenty záhlaví a zápatí v šabloně se automaticky zobrazí na každé navazující stránce.)

- Zachovejte podnikové weby ve schváleném vzhledu definováním sady uspořádání modulů a možností konfigurace.

    > [!TIP] 
    > Úspěšné weby e-Commerce poskytují zákazníkům známé, opakovatelné firemní vzory návrhu (UX). Pomocí šablon můžete ovládat konzistenci v celém webu.

- Zvyšte skóre optimalizace vyhledávače (SEO) tak, že zaručíte opakované a programově definované definice stránek a metadata.

> [!NOTE]
> Ačkoli jsou šablony navrženy za účelem kontroly konzistence v rámci webu, mohou teoreticky být nakonfigurovány tak, aby nevynucují žádnou konzistenci. Značka a správci webu mohou definovat libovolnou úroveň proměnlivosti stránek na webu. Šablona může například být ponechána zcela otevřená, takže autoři obsahu mohou vytvářet libovolné návrhy stránek, které zvolí. V tomto případě se nepoužije žádná z výhod uvedených v předchozím seznamu.

## <a name="modify-a-template"></a>Úprava šablony

Šablony jsou upravovány pomocí editoru šablon.

Chcete-li otevřít editor šablon, postupujte jedním z následujících kroků:

- V navigačním podokně webu vyberte možnost **Šablony** a poté vyberte šablonu, kterou chcete upravit.
- V editoru stránek pro existující stránku vyberte horní uzel ve stromu osnovy vlevo. Potom v podokně vlastností vpravo vyberte vlastnost **Upravit šablonu**.

V zobrazení stromové struktury osnovy na levé straně jsou zobrazeny možnosti modulu a struktury, které jsou k dispozici pro podřízené rozložení a stránky. Vyberete-li modul ve stromu osnovy, můžete zobrazit vlastnosti šablony pro vybraný modul v podokně vlastností vpravo. Některé z těchto vlastností jsou jedinečné pro úpravy šablony. Následující tabulka obsahuje popis vlastností.

| Název vlastnosti | Popis |
|---|---|
| Min. počet výskytů | Tato vlastnost definuje minimální počet výskytů pro vybraný modul. Je-li například hodnota nastavena na **1**, modul je povinný pro navazující autory, zatímco pokud je hodnota nastavena na **0** (nula). modul je nepovinný. |
| Max. počet výskytů | Tato vlastnost definuje maximální počet výskytů pro vybraný modul. Je-li například hodnota nastavena na **1**, lze modul přidat pouze jednou. |
| Min. moduly (kontejnery) | V modulech, které obsahují jiné moduly (tj. *moduly kontejnerů*), definuje tato vlastnost minimální počet všech modulů, které by měly být přidány jako podřízené. Například pro modul karusel může být hodnota nastavena na číslo, které je větší než 1. |
| Max. moduly (kontejnery) | U modulů kontejnerů tato vlastnost definuje maximální počet modulů celkem, které by měly být přidány jako podřízené. Například pro modul karusel může být hodnota nastavena na číslo, které je menší než 10. |
| Uzamčeno | **Zamčený** ovládací prvek logické hodnoty se zobrazí vedle všech vlastností základního modulu. To umožňuje autorovi šablony zamknout nastavení modulu v šabloně. Zamknuté nastavení modulu nelze přepsat žádnými podřízenými rozloženími nebo stránkami. Stane se centrálně upravitelnou hodnotou vlastnosti pro všechna rozložení a stránky, které šablonu používají. |

## <a name="create-a-new-template"></a>Vytvořte novou šablonu

Při vytváření nové šblony postupujte takto.

1. V navigačním podokně webu vyberte možnost **Šablony**, chcete-li otevřít zobrazení inspektoru šablon.
1. vyberte **Nová šabllona**.
1. V dialogovém okně pro vytvoření šablony zadejte název a popis šablony. Zadané hodnoty se zobrazí autorům při vytváření nových stránek. Zadejte proto metadata, která budou užitečná pro autory stránek. Například zadejte jako popis **Použijte tuto šablonu k vytvoření obecných marketingových stránek**. Tato metadata lze upravit později.
1. Chcete-li vytvořit novou šablonu a otevřít editor šablon, klepněte na tlačítko **OK**. Editor šablon zobrazuje strom osnovy vlevo a podokno vlastností vpravo.
1. Ve stromové struktuře osnovy rozbalte uzly a vyberte slot **Záhlaví HTML**.
1. Pokud v této patici ještě nejsou žádné moduly, vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul.**
1. V dialogovém okně **Přidat modul** vyberte **Výchozí souhrn stránky** a pak vyberte možnost **OK**.
1. Ve stromu osnovy vyberte nový modul a poté v podokně vlastností zadejte všechna výchozí nastavení, která mají být automaticky konfigurována pro všechny podřízené stránky šablony. Pokud nechcete žádné výchozí nastavení, ponechte hodnoty prázdné.
1. Ve stromové struktuře vyberte slot **Obsah**, vyberte tlačítko se třemi tečkami a vyberte možnost **Přidat modul**.
1. Vyberte modul kontejneru stránky (může existovat pouze jedna možnost) a pak klepněte na tlačítko **OK.**

V modulu kontejnerů nové stránky se zobrazí nová sada slotů (**Záhlaví**, **hlavní** atd.). Zde můžete přidat a nakonfigurovat možnosti modulu, které budou k dispozici autorům při vytváření stránek z této šablony. Pokud ve výchozím nastavení nepřidáte žádné moduly do slotu, budou pro tento slot podporovány všechny dostupné typy modulů.

Šablona je nyní technicky platná a lze ji uložit, vrátit se změnami a použít k vytvoření nových stránek. Následující tři oddíly však popisují některá další výchozí nastavení, která je vhodné nakonfigurovat jako první.

## <a name="add-a-header-and-a-footer"></a>Vložení záhlaví a zápatí

Pokud již na webu existuje fragment záhlaví, přidejte pomocí následujícího postupu záhlaví a zápatí do šablony.

1. Ve stromu osnovy rozbalte oblast **Obsah** a její podřízený modul stránky.
1. Vyberte slot **Záhlaví**.
1. Vyberte tlačítko se třemi tečkami (...) pro slot **Záhlaví** a poté vyberte možnost **Přidat fragment**.
1. Vyhledejte a vyberte fragment záhlaví vašeho webu a poté klepněte na tlačítko **OK**.

Všechny stránky, které používají tuto šablonu, budou automaticky dědit tento fragment záhlaví.

Pokud váš web dosud neobsahuje fragment záhlaví, vyhledejte informace o [Vytvoření fragmentu](work-with-fragments.md#create-a-fragment) a potom dokončete předchozí postup.

## <a name="change-the-template-theme"></a>Změna motivu šablony

Chcete-li nastavit výchozí motiv pro všechny stránky používající šablonu, postupujte následujícím způsobem.

1. Ve stromu osnovy stránky nalevo rozbalte slot **Hlavní část**.
1. Ve slotu **Hlavní obsah** vyberte modul kontejneru stránky (například **Výchozí stránka**).
1. V podokně vlastností vpravo v poli **Motiv** vyberte motiv.

Ve výchozím nastavení budou nyní všechny nové stránky používat vybraný motiv. Chcete-li zabránit, aby stránky přepsaly toto nastavení na úrovni rozvržení nebo stránky, nastavte logický ovládací prvek **Zamčeno** na hodnotu **True**.

## <a name="add-a-script-to-a-template"></a>Přidání skriptu do šablony

Do šablony můžete přidat prvky **&lt;skriptu&gt;** HTML, které obsahují JavaScript. Tímto způsobem můžete poskytnout výchozí chování skriptu k záhlaví HTML, začátku hlavního obsahu a konce základního obsahu na vašich sránkách.

Chcete-li přidat skript do šablony, postupujte takto.

1. Ve stromu osnovy vlevo vyberte slot, do něhož chcete přidat prvek **&lt;skriptu&gt;** (například záhlaví HTML, začátek hlavního obsahu či konec hlavního obsahu).
1. Vyberte tlačítko se třemi tečkami pro slot a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte skriptovací modul (například **Externí skript** nebo **Vložený skript**).
1. V podokně vlastností vpravo v příslušném ovládacím prvku vlastnosti skriptu (například **vložený skript** nebo **značky skriptu**) zadejte požadovaný skript.
1. V podokně vlastností zadejte další volitelná nastavení, která chcete konfigurovat.

> [!TIP]
> Chcete-li znovu použít kterýkoli z skriptovacích modulů pro jiné šablony, můžete je převést na fragmenty. Tímto způsobem můžete zvýšit efektivitu procesu tvorby a centralizovat proces aktualizace. Informace o tom, jak převést skriptovací modul na fragment, naleznete v tématu [Uložení existující konfigurace modulu jako fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>Uložení, navrácení se změnami, náhled a publikování šablony

Chcete-li uložit a vrátit se změnami šablonu, postupujte následujícím způsobem.

1. V horní části editoru šablon vyberte **Uložit**. Uložené změny nemají vliv na navazující stránky, dokud nejsou vráceny se změnami.
1. Vyberte **Dokončit úpravy**. Vaše změny jsou nyní zjistitelné pro navazující workflowy.

Chcete-li zobrazit náhled změn, buď otevřete existující stránku, která používá šablonu, nebo vytvořte novou stránku z šablony.

Po zobrazení náhledu změn vašich šablon můžete publikovat šablonu na aktivním webu podle jednoho z následujících kroků:

* Přejděte na **Šablony**, vyberte šablonu a poté vyberte možnost **Publikovat**.
* Vyberte název rozvržení pro otevření editoru rozložení a pak vyberte **Publikovat**.
* Publikujte stránku, která odkazuje na nepublikovanou šablonu. Šablona je automaticky publikována.

> [!WARNING]
> Pokud je publikována šablona nebo jakákoli jiná položka systému správy obsahu (CMS), je zjistitelná na internetu. Nepublikujte dokumenty nebo materiály, dokud je nebudete moci zveřejnit. Verze dokumentů, které byly uloženy a vráceny se změnami, ale dosud nebyly publikovány, jsou zjistitelné pouze pro ověřené uživatele systému.

## <a name="additional-resources"></a>Další zdroje

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Práce s přednastavenými rozloženími](work-with-layouts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]