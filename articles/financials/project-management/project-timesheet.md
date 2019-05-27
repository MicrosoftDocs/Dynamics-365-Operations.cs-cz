---
title: Mobilní aplikace časového rozvrhu projektu
description: Toto téma obsahuje informace o mobilní aplikaci Microsoft Dynamics 365 Project Timesheet Mobilní aplikace Project Timesheet umožňuje uživatelům odeslání a schválení časových rozvrhů projektů na jejich mobilních zařízeních.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a475085001b8fa10814c864ef35129eb6ebfdfef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529872"
---
# <a name="microsoft-dynamics-365-project-timesheet-mobile-application"></a>Mobilní aplikace Microsoft Dynamics 365 Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Přehled

Mobilní aplikace Microsoft Dynamics 365 Project Timesheet umožňuje uživatelům odeslání a schválení časových rozvrhů projektů na jejich mobilních zařízeních (iPhone nebo Android). Tato mobilní aplikace je vybavena funkcí časového rozvrhu, která je umístěna v Řízení projektů a účetnictví aplikace Microsoft Dynamics 365 for Finance and Operations a zlepšuje produktivitu a efektivitu uživatelů a umožňuje včasné zadávání a schvalování časového rozvrhu projektu.

## <a name="download-and-install-the-mobile-app"></a>Stáhněte a nainstalujte mobilní aplikaci

Stáhněte si a nainstalujte mobilní aplikaci Microsoft Dynamics 365 Project Timesheet pro Android nebo iPhone pro své zařízení z obchodu s mobilními aplikacemi.

## <a name="enable-the-app"></a>Povolení aplikace 

V aplikaci Dynamics 365 for Finance and Operations musí být povolena mobilní aplikace Project Timesheet. Chcete-li funkci povolit, přejděte na **Parametry modulu Řízení a účetnictví projektu \> Časový rozvrh** a vyberte parametr **Povolit Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Přihlášení do aplikace

1.  Spusťte aplikaci na svém mobilním zařízení.

2.  Zadejte URL adresu Microsoft Dynamics 365 for Finance and Operations.

3.  Při prvním přihlášení se zobrazí výzva k zadání uživatelského jména a hesla. Zadejte své přihlašovací údaje.

4.  Budete přihlášení do své výchozí společnosti.

## <a name="submit-a-project-timesheet"></a>Odeslání časového rozvrhu projektu

Můžete vytvořit a odeslat časový rozvrh projektu v aplikaci. Můžete také založit nový časový rozvrh na informacích z dřívějšího časového rozvrhu, uložených řádcích nebo přiřazeních projektů. Pokud jste zvoleni jako delegát, můžete také zadat časový rozvrh pro jiného pracovníka. K vytvoření časového rozvrhu jako delegát vyberte tlačítko **Nabídka** a pak vyberte název zdroje.

Stránka časového rozvrhu vytvoří nový časový rozvrh pro období časového rozvrhu na základě aktuálního data. Zobrazí se pracovní týden. Jestliže období časového rozvrhu zahrnuje několik týdnů, můžete vybrat další pracovní týden z karet pracovních týdnů.
Pokud časový rozvrh existuje pro aktuální datum, zobrazí se. Pokud je nutné vytvořit nový časový rozvrh v různých obdobích časových rozvrhů, vyberte tlačítko **Nabídka** a vyberte **Nový časový rozvrh**.

Můžete zadat informace o projektu kliknutím na akci **Přidat čas** nebo **Kopírovat čas z**. Akce **Kopírovat čas z** zkopíruje informace o řádku projektu, nikoliv však hodiny. Nabídka **Kopírovat čas z** obsahuje následující možnosti:

- **Kopírovat z existujícího časového rozvrhu** -kopírování řádků časového rozvrhu z existujícího časového rozvrhu.

- **Kopírovat z oblíbených položek** – vytvoří nové řádky časového rozvrhu pomocí nastavení časového rozvrhu, které jste vybrali jako oblíbené.

- **Kopírovat z přiřazení** – vytvoří nové řádky časového rozvrhu z přiřazených projektů.

Zobrazené informace o projektu jsou závislé na mobilních parametrech, které jste definovali na stránce **Parametry modulu Řízení a účetnictví projektu**.

V poli **Právnická osoba** vyberte právnickou osobu, pro kterou jste prováděli práce na projektu. Pole **Právnická osoba** je k dispozici pouze v případě, že vaší právnické osobě je povolena podpora mezipodnikových časových rozvrhů.

Vyberte odběratele, který je přidružený k projektu pro časový rozvrh. Pro počáteční verzi na systému Android není podporováno zadání odběratelem, protože je nutné nejprve vybrat projekt. Pokud jste vybrali nejprve projekt, pole **Odběratel** se vyplní automaticky.

V poli **Projekt** vyberte projekt, pro který zadáváte čas. Pole **Odběratel** se vyplní automaticky.

Vyhledávání odběratele a projektu umožňuje hledání napříč odběrateli i projekty.

Vyberte informace v polích **Kategorie**, **Aktivita**, **Vlastnost řádku**, **Skupina DPH** a **Skupina DPH položky** podle potřeby. Tato pole lze přepsat.

Pole **Vlastnost řádku** bude nastaveno na výchozí hodnotu, na základě parametrů řízení a účetnictví projektu. Jsou-li parametry projektu/kategorie a kategorie/zdroje povoleny, hodnota **Vlastnost řádku** bude nastavena na výchozí hodnotu, kterou jste definovali pro toto ověření. Nejsou-li parametry projektu/kategorie a kategorie/zdroje povoleny, hodnota **Vlastnost řádku** bude nastavena na výchozí podle pole **Povolit výchozí vlastnost řádku** na stránce **Parametry modulu Řízení a účetnictví projektu**. Hodnotu **Vlastnost řádku** lze přepsat.

Zvolte datum pro přidání času. Zadejte počet odpracovaných hodin za každý den.

Pro přidání komentářů k hodinám, které zadáváte, klikněte na **Přidat komentáře** a zadejte komentáře pro interní cílovou skupinu, cílovou skupinu odběratelů nebo obě.
Interní komentáře mohou zobrazit pouze projektoví manažeři. Komentáře odběratele jsou zahrnuty na fakturách.

Řádek můžete uložit do oblíbených položek zaškrtnutím políčka a kliknutím na položku **Uložit jako oblíbené**.

Finanční dimenze a podpora příloh nejsou v mobilní aplikaci poskytovány.

Pokračujte v přidávání řádků projektu podle potřeby pro dokončení časového rozvrhu.

Kliknutím na tlačítko **Odeslat** odešlete časový rozvrh do workflowu schválení.

## <a name="review-timesheets"></a>Kontrola časových rozvrhů

Seznam časových rozvrhů, které je třeba zkontrolovat, je k dispozici v nabídce. Tato možnost je k dispozici pouze v případě, když jste určili schvalovatele workflow. Jsou podporována schválení řádku i záhlaví. Schválení na úrovni řádku nabízí možnost označit jeden nebo více řádků ke schválení. Po kontrole informací o časovém rozvrhu klikněte na **Schválit**, **Delegovat**, nebo **Vrátit** pro pokračování ve workflow.
