---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (3. března 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fdd409b33989e371d0bd2a6e21b27721336cea0
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2020
ms.locfileid: "3114420"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (3. března 2020)

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.2955. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Řešení Common Data Service je nyní k dispozici s následujícími změnami:

Nové řešení Common Data Service bude brzy k dispozici po provedení následujících změn:

| Popis | Změna |
| ----------------------------------------- | --- |
| Změny entity **práce/pozice** | Přidána **Oblast kompenzace**</br>Přidání **finančních dimenzí** |
| Změny entity **pracovníka** | Přidání **sekvence jmen**</br>Přidaná možnost **Práce z domova**</br>Přidán **jazyk**</br>Přidáno **Datum služebního věku**</br>Přidáno **Datum výročí**</br>Přidáno **Datum původního přijetí** |
| Změny **entity zaměstnání** | Přidání **finančních dimenzí**</br>Přidán **Důvod pro výpověď**</br>**Datum ukončení** přejmenováno z **data přechodu**</br>Přidáno **datum zkušební doby** |
| Změny entity **adresy pracovníka** | Přidána **Adresa ulice**</br>**Řádek adresy 1**, **řádek adresy 2** a **řádek adresy 3** označené pro odpis |
| Nové entity nastavení s nastavením variabilní kompenzace | **Typ plánu variabilní kompenzace**</br>**Plán variabilní kompenzace**</br>**Pravidla připsání**</br>**Úroveň plánu variabilní kompenzace** |
| Nová entita **Zaměstnání dle kalendáře pracovníka** | Byla přidána **entita pracovního kalendáře** |
| Nová entita **Mzdové podrobnosti o pozici** | Byla přidána položka **Mzdové podrobnosti o pozici**. |
| Nová entita **Pozice** | Byla přidána položka **Pozice**. Nová entita **Nadpis** bude zahrnuta do procesu synchronizace mezi lidskými zdroji a Common Data Service. Na počátku nebude odkazovat z entit **Pracovní pozice** nebo **Úloha**. |

Během příštích několika týdnů budou tyto změny entit k dispozici ve všech prostředích. Postup při ruční instalaci nejnovějšího řešení Common Data Service pro Human Resources:

1.  Přejděte do [Centra pro správu Power Platform](https://admin.powerplatform.microsoft.com).

2.  Vyberte **Prostředí**.

3.  Vyhledjete prostředí, která chcete upgradovat. Prostředí by mělo odpovídat poli **Název prostředí** v sekci **Informace o Common Data Service** ve formuláři **O aplikaci** v modulu Human Resources.

4.  Vyberte prostředí pro zobrazení podrobností o prostředí.

5.  Vyberte možnost **Správa řešení** na panelu akcí nahoře. Otevře se nové okno prohlížeče a přejde do **Centra pro správu Dynamics 365** v kontextu vašeho prostředí.

6.  Na seznamu **Řešení** vyberte možnost **Kotva Dynamics 365 Human Resources**.

7.  Chcete-li použít poslední řešení, vyberte možnost **Upgrade**.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Problémy s importem datové entity pro přihlášení pracovního volna (406082)

Nyní můžete zaměstnance přihlásit do nového plánu pracovního volna stejného typu, pokud je nové datum přihlášení pozdější než datum přihlášení s vypršenou platností předchozího plánu.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Problém s exportem sazeb příspěvků v entitě 401k payrollWorkerEnrolledBenefitDetail v DMF (420700)

Tato změna opraví funkci exportu pro entitu **payrollWorkerEnrolledBenefitDetail** tak, aby odrážela aktuální hodnoty příspěvku zaměstnavatele.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Vyhledávání ve zjednodušeném formuláři Pracovník způsobuje zprávu, že je nutné vyplnit pole Osoba (402525)

Při hledání zaměstnance se již nebude zobrazovat zpráva, že je nutné vyplnit pole **Osoba**.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Hodnota pole poznámky se nevykreslí ve formuláři Přidat další dovednosti (380134)

Tato změna opravuje problém, když přizpůsobíte formulář **Přidat další dovednosti** v samoobsluze pro zaměstnance.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Při převodu zaměstnanců nevyprší více plánů fixní kompenzace (389466)

Při této změně vyprší platnost všech aktivních záznamů fixní kompenzace pro starou pozici k datu převodu.

## <a name="in-preview"></a>Náhled

Od 3. února 2020 budou k dispozici následující ukázkové funkce:

- **Funkce náhledu o pracovním volnu a absenci** Další informace získáte v části [Funkce náhledu o pracovním volnu a absenci](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Funkce náhledu správy zaměstnaneckých výhod** - Další informace, včetně známých problémů, získáte v části [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md).