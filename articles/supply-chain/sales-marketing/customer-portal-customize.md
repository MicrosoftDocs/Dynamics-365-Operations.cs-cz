---
title: Přizpůsobení a použití zákaznického portálu
description: Toto téma vysvětluje, jak přizpůsobit zákaznický portál poté, co byl přidán do vašeho systému.
author: Henrikan
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 02ad0470b7886b2e9b259682a7f8c8150d656cfb
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063486"
---
# <a name="customize-and-use-the-customer-portal"></a>Přizpůsobení a použití zákaznického portálu

[!include [banner](../includes/banner.md)]


Toto téma popisuje různé stránky, které jsou ihned k dispozici na zákaznickém portálu. Vysvětluje, co stránky dělají a jak je můžete přizpůsobit.

Zákaznický portál nabízí ihned několik webových stránek a akcí. Následující mapa webu poskytuje přehled těchto webových stránek a akcí a rolí, které mohou akce provádět.

![Mapa webu zákaznického portálu.](media/customer-portal-site-map.png "Mapa webu zákaznického portálu")

## <a name="typical-customizations"></a>Typické úpravy

Následující témata vám pomohou naučit se základy Power Apps portálů a jak můžete portály přizpůsobit:

- [Práce se šablonami](/powerapps/maker/portals/work-with-templates) - Toto téma poskytuje obecný přehled o tom, jak Power Apps portály fungují a jak můžete provádět jednoduché přizpůsobení portálů.
- [Správa obsahu portálu](/dynamics365/portals/manage-portal-content) - Toto téma vysvětluje, jak můžete spravovat a přizpůsobovat obsah, který se objeví na vašem portálu.
- [Upravit CSS](/powerapps/maker/portals/edit-css) - Toto téma vám pomůže provádět složitější úpravy uživatelského rozhraní (UI) vašeho portálu.
- [Vytvořte téma pro svůj portál](/dynamics365/portals/create-theme) - Toto téma vám pomůže vytvořit motiv uživatelského rozhraní pro váš portál.
- [Vytvářejte a exponujte obsah portálu snadno](/dynamics365/portals/create-expose-portal-content) - Toto téma vám pomůže spravovat základní data a tabulky, které používáte pro svůj portál.
- [Nakonfigurujte kontakt pro použití na portálu](/powerapps/maker/portals/configure/configure-contacts) - Toto téma vysvětluje, jak vytvářet a přizpůsobovat uživatelské role a jak funguje zabezpečení a ověřování Power Apps portálů.
- [Nakonfigurujte poznámky pro formuláře tabulky a webové formuláře na portálech](/powerapps/maker/portals/configure-notes) - Toto téma vysvětluje, jak přidat dokumenty a další úložiště na váš portál.
- [Chyba při manipulaci s webovým portálem](/powerapps/maker/portals/admin/view-portal-error-log) - Toto téma vysvětluje, jak zobrazit protokoly chyb portálu a uložit je do vašeho účtu úložiště blob Microsoft Azure.

## <a name="customize-the-order-creation-process"></a>Přizpůsobte proces vytváření objednávek

Když uživatel odešle objednávku pomocí zákaznického portálu, objednávka se automaticky synchronizuje s odpovídajícím prostředím Dynamics 365 Supply Chain Management. Protože je uživatel externím zákazníkem, některé požadované informace jsou před ním úmyslně skryty. Tato informace bude automaticky vyplněna při odeslání formuláře.

Tato část ukazuje, jak byste měli nastavit kontakty, abyste se vyhnuli chybám. Vysvětluje pole, která jsou automaticky nastavena a jak můžete upravit hodnotu těchto polí, pokud je to nutné.

### <a name="the-out-of-box-order-creation-process"></a>Dodávaný proces vytváření objednávek

Zde jsou standardní kroky pro odeslání objednávky ze zákaznického portálu.

1. Na domovské stránce vyberte dlaždici **Vytvořit objednávku** otevření průvodce **Vytvořit objednávku**.
1. Na stránce **Informace o objednávce** zadejte následující pole:

    - **Požadované datum přijetí** - Určete datum doručení.
    - **Doručovací adresa** - Zadejte adresu, na kterou má být objednávka doručena.
    - **Společnost** - Vyberte název zákaznické společnosti. Toto pole je automaticky nastaveno pro neadministrátorské uživatele.
    - **Číslo žádosti** - Zadejte číslo žádosti o objednávku. Toto pole není povinné.
    - **Odeslat do země / oblasti** - Zadejte zemi nebo region, do kterého budou položky doručeny. Toto pole je automaticky nastaveno pro neadministrátorské uživatele.

    ![Stránka s informacemi o objednávce.](media/customer-portal-order-information.png "Stránka s informacemi o objednávce")

1. Zvolte **Další**.
1. Na stránce **Položky** vyberte **Přidat položku**.

    ![Stránka položek.](media/customer-portal-items.png "Stránka položek")

1. V dialogovém okně **Informace o položce** nastavte následující pole:

    - **jméno výrobku** - Najděte a vyberte produkt, který chcete přidat do objednávky.
    - **Množství** - Zadejte množství vybraného produktu.
    - **Jednotka** - Určete měrnou jednotku (například **ks**, **kg** nebo **krabice**).
    - **Odhadovaná čistá částka** - Hodnota se vypočítá jako odhadovaná cena položky × množství pro vybranou jednotku.

    ![Dialogové okno Informace o položce.](media/customer-portal-item-information.png "Dialogové okno Informace o položce")

1. Vyberte **Odeslat** a přidejte položku do objednávky.
1. Opakujte kroky 4 až 6, dokud nepřidáte všechny položky, které chcete objednat.
1. Po dokončení přidávání položek vyberte **Další** na stránce **Položky**.
1. Stránka **Informace o objednávce** obsahuje shrnutí objednávky. Zkontrolujte obsah objednávky a podrobnosti o doručení. Pokud vše vypadá správně, vyberte **Odeslat** k odeslání objednávky.

    ![Stránka s informacemi o dokončené objednávce.](media/customer-portal-order-submit.png "Stránka s informacemi o dokončené objednávce")

### <a name="standard-data-setup"></a>Standardní nastavení dat

Aby byl zajištěn hladký uživatelský dojem, portál pro zákazníky automaticky vyplňuje hodnoty pro několik požadovaných polí. Tyto hodnoty vycházejí z informací v kontaktním záznamu zákazníka, který zadává objednávku.

Pro každý [záznam řádku](/powerapps/maker/portals/configure/configure-contacts) patřící zákazníkovi, který bude používat zákaznický portál k zadávání objednávek, je nutné zadat hodnoty pro následující povinná pole. Jinak dojde k chybám.

- **Společnost** – Právnická osoba, které náleží objednávka
- **Potenciální zákazník** - Účet odběratele přidružený k objednávce
- **Ceník** - Vlastní ceník pro zákazníka
- **Měna** - Měna ceny
- **Odeslat do země / oblasti** - Země nebo region, do kterého budou položky doručeny

Pro tabulku prodejní objednávky jsou automaticky nastavena následující pole:

- **Jazyk** - Jazyk objednávky (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)
- **Odeslat do země / oblasti** - Země nebo region, do kterého budou položky doručeny (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)
- **Kontaktní osoba** - Uživatel, kterého lze kontaktovat pro informace o objednávce (Ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)
- **Společnost** - Právnická osoba, které objednávka patří (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)
- **Potencionální zákazník** - Zákaznický účet, který je přidružen k objednávce (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)
- **Zákazník na faktuře** - fakturační účet objednávky (ve výchozím nastavení je to potenciální zákazník z kontaktního záznamu.)
- **Název prodejní objednávky** - Název prodejní objednávky (Výchozí hodnota je **prodejní objednávka** .)
- **Měna** - Měna ceny (ve výchozím nastavení je hodnota převzata z kontaktního záznamu.)
- **Ceník** - Vlastní ceník pro zákazníka (Standardně je hodnota převzata z kontaktního záznamu.)
- **Popis dodací adresy** - dodací adresa prodejní objednávky (výchozí hodnota je **popis dodací adresy** .)

### <a name="modify-the-order-creation-process"></a>Upravte proces vytváření objednávek

Pokud nezměníte základní proces vytváření objednávek, můžete libovolně upravovat vzhled a uživatelské rozhraní zákaznického portálu. Pokud chcete změnit proces vytváření objednávek, musíte mít na paměti několik bodů.

Neodstraňujte následující sloupce z tabulky prodejní objednávky v Microsoft Dataverse, protože musí vytvořit prodejní objednávku v režimu dvojitého zápisu:

- **Společnost** – Právnická osoba, které náleží objednávka
- **Název** – název prodejní objednávky
- **Měna** - Měna ceny
- **Ceník** - Vlastní ceník pro zákazníka
- **Odeslat do země / oblasti** - Země nebo region, do kterého budou položky doručeny
- **Potenciální zákazník** - Účet odběratele přidružený k objednávce
- **Jazyk** - Jazyk objednávky (Obvykle je tento jazyk jazykem potenciálního zákazníka.)
- **Popis dodací adresy** - dodací adresa prodejní objednávky

U položek jsou požadovány následující sloupce:

- **Produkt** - Produkt k objednání
- **Množství** - množství vybraného produktu
- **Jednotka** - Měrná jednotka (například **ks**, **kg** nebo **krabice**)
- **Odeslat do země / oblasti** - Země nebo oblast doručení
- **Popis dodací adresy** - dodací adresa objednávky

Musíte se ujistit, že váš zákaznický portál nějak předá hodnoty pro všechny tyto sloupce.

Chcete-li na stránku přidat sloupce nebo je odstranit, viz [Vytvářejte nebo upravujte rychle vytvářené formuláře pro efektivnější zadávání dat](/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).

Pokud chcete změnit, jak jsou sloupce přednastaveny a jak jsou hodnoty nastaveny při uložení stránky, podívejte se na následující informace v dokumentaci portálů Power Apps:

- [Předem vyplněné pole](/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [Nastavit hodnotu při uložení](/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a>Přizpůsobte domovskou stránku

Všechny ovládací prvky v zákaznickém portálu jsou vestavěné ovládací prvky portálů Power Apps. Můžete je upravit podle kroků v článku [Vytvořte stránku](/powerapps/maker/portals/compose-page) v dokumentaci portálů Power Apps.

Jediný vlastní ovládací prvek, který je součástí šablony zákaznického portálu, se používá k vytvoření dlaždic na domovské stránce.

![Dlaždice na domovské stránce.](media/customer-portal-home-page-tiles.png "Dlaždice na domovské stránce")

Chcete-li upravit dlaždice, postupujte takto.

1. Otevřete [Aplikaci pro správu portálu](/powerapps/maker/portals/configure/configure-portal).
1. V navigačním podokně nalevo vyberte položku **Šablony stránky**.

    ![Navigační podokno správy portálu.](media/customer-portal-nav.png "Navigační podokno správy portálu")

1. Vyberte šablonu stránky s názvem **Domov**.
1. V poli **Webová šablona** vyberte okaz **Domov** pro otevření zdrojového kódu pro tuto stránku.

    ![Pole webové šablony.](media/customer-portal-web-template.png "Pole webové šablony")

1. Nyní byste měli vidět veškerý zdrojový kód domovské stránky a můžete jej podle potřeby upravit.

## <a name="resources"></a>Prostředky

Další informace o tom, jak můžete nastavit a přizpůsobit zákaznický portál, naleznete v následujících zdrojích:

- [Dokumentace portálů Power Apps](/powerapps/maker/portals/overview)
- [Dokumentace dvojitého zápisu](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [O životním cyklu portálu](/powerapps/maker/portals/admin/portal-lifecycle)
- [Upgradujte portál](/powerapps/maker/portals/admin/upgrade-portal)
- [Migrace konfigurace portálu](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Správa životního cyklu řešení: aplikace Dynamics 365 for Customer Engagement](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]