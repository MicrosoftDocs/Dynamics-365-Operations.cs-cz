---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (21. ledna 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c0c303ec5d009fce0c975eb797f018b5e27a41eb
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982400"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Talent (21. ledna 2020)

[!include [banner](includes/banner.md)]

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract. Do aplikace Attract jsme přidali funkci na podporu našeho nedávného oznámení [Budování úspěšnějších pracovních sil pomocí Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>Stáhnout data prostředí

Správci si mohou stáhnout data o svém prostředí. Data jsou exportována ve standardním formátu JSON se všemi úlohami, kandidáty a konfigurací exportovanými v souboru ZIP. Další informace naleznete v tématu [Export dat z Attract a Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Omezení přístupu k prostředí pro uživatele, kteří nejsou správci

Správci mohou nyní omezit přístup k prostředí pro uživatele, kteří nejsou správci. Tuto akci nelze vrátit zpět. Další informace naleznete v tématu [Omezení přístupu do aplikace Attract](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>Export průvodců zaškolením

Uživatelé nyní mohou exportovat všechny své průvodce zaškolení a šablony zaškolení ve formátu dokumentu aplikace Word. Další informace naleznete v tématu [Export dat z Attract a Onboard](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2726. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Poslední pole roční kompenzace ve formuláři Ověřit zaměstnání není konzistentní (392092).

Tato verze obsahuje změnu, která bude konzistentně zobrazovat poslední měnu na základě výběru společnosti ve formuláři **Ověřit zaměstnání**.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Známé jako pole přidané do vyhledávání příjemce zpětné vazby (407789)

Při poskytování zpětné vazby k výkonu neposkytlo vyhledávání pracovníkům dostatek informací pro určení, zda zpětná vazba jde správnému uživateli. Přidali jsme sloupec **Známý jako**, který vám pomůže identifikovat jedinečné jméno zaměstnance.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>Záznam HcmWorkerPayrollInfo je vytvořen bez přidružení pracovníka (394526).

Tato verze obsahuje změnu, která nezapisuje záznamy HCMWorkerPayrollInfo, aniž by odkazovala na zaměstnance.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Možnost úpravy oddělení při navigaci z hierarchie pozic (341001)

Pokud byla zabezpečení nastavena tak, aby odepřela přístup k oddělením pro úpravy, budou úpravy při přechodu do formuláře **oddělení** ve všech scénářích zakázány.

## <a name="coming-soon"></a>Již brzy

Nové řešení Common Data Service bude brzy k dispozici po provedení následujících změn:

| Popis | Změna |
| --- | --- |
| Změny entity **práce/pozice** | <ul><li>Přidána **Oblast kompenzace**</li><li>Přidání **finančních dimenzí**</li></ul> |
| Změny entity **pracovníka** | <ul><li>Přidání **sekvence jmen**</li><li>Přidaná možnost **Práce z domova**</li><li>Přidán **jazyk**</li><li>Přidáno **Datum služebního věku**</li><li>Přidáno **Datum výročí**</li><li>Přidáno **Datum původního přijetí**</li></ul> |
| Změny **entity zaměstnání** | <ul><li>Přidání **finančních dimenzí**</li><li>Přidán **Důvod pro výpověď**</li><li>**Datum ukončení** přejmenováno z **data přechodu**</li><li>Přidáno **datum zkušební doby**</li></ul> |
| Změny entity **adresy pracovníka** | <ul><li>Přidána **Adresa ulice**</li><li>**Řádek adresy 1**, **řádek adresy 2** a **řádek adresy 3** označené pro odpis</li></ul> |
| Nové entity nastavení s nastavením variabilní kompenzace | <ul><li>**Typ plánu variabilní kompenzace**</li><li>**Plán variabilní kompenzace**</li><li>**Pravidla připsání**</li><li>**Úroveň plánu variabilní kompenzace**</li></ul> |
| Nová entita **Zaměstnání dle kalendáře pracovníka** | <ul><li>Byla přidána **entita pracovního kalendáře**</li></ul> |
