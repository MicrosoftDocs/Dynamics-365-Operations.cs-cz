---
title: Glosář modelu stránky
description: V tomto článku jsou popsány různé prvky používané na stránkách webu Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: a4c2a29e8c2112622b5e30064e26523b4f9e2d5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281420"
---
# <a name="page-model-glossary"></a>Glosář modelu stránky


[!include [banner](includes/banner.md)]

V tomto článku jsou popsány různé prvky používané na stránkách webu Microsoft Dynamics 365 Commerce.

## <a name="page-element-definitions"></a>Definice prvků stránky

V následující tabulce je uveden přehled termínů, které byste měli znát při změně vzhledu, dojmu a obsahu vašeho webu. Podrobnější vysvětlení a postupy získáte pomocí odkazů.

| Termín | Popis a poznámky |
|------|-----------------------|
| [Modul](work-with-modules.md) | <p>**Definice:** moduly jsou stavebními bloky, které lze vytvářet a které tvoří kostru webové stránky. Příkladem jsou moduly záhlaví, prémiový a karusel.</p><p>**Kde je vybráno:** nasazené moduly lze vybrat a konfigurovat v různých fázích pracovního postupu vytváření webů, jako je například šablona, rozložení, stránka a fáze vytváření fragmentů.</p><p>**Kde je upravováno:** vlastní moduly jsou vytvořeny v kódu pomocí sady SDK (Software Development Kit). Poté jsou odeslány na váš web, kde budou k dispozici pro výběr.</p> |
| Vlastnost modulu | <p>**Definice:** vlastnosti modulu jsou specifická nastavení, která jsou definována v modulu. Lze je upravit v nástrojích pro vytváření e-Commerce. Vlastnosti modulu se například používají k nastavení záhlaví a obrázku pozadí modulu banneru.</p><p>**Kde je konfigurováno:** vlastnosti modulu jsou vybrány a konfigurovány v podokně vlastností, které se zobrazí ve vývojovém prostředí (editory) pro šablony, rozložení, stránky, fragmenty a nastavení aplikace.</p> |
| [Šablona](templates-layouts-overview.md) | <p>**Definice:** šablony definují kombinace a možnosti modulu, které by měly být použity pro určitou kategorii stránek (například marketingové stránky, stránky kategorií a stránky produktů).</p><p>**Kde je vybráno:** šablony lze vybrat během pracovních postupů vytváření stránek nebo rozložení.</p><p>**Kde je upravováno:** šablony jsou vytvořeny v editoru šablon. K vytvoření nebo úpravě není nutné žádný kód.</p> |
| [Rozvržení](templates-layouts-overview.md) | <p>**Definice:** rozvržení definují finální výběr a uspořádání modulů z nadřazené šablony sadou možností. Rozvržení lze konfigurovat pro jednu stránku (*vlastní rozložení*) nebo může být sdíleno více stránkami (*přednastavené rozvržení*).</p><p>**Kde je vybráno:** rozvržení lze vybrat při vytváření nové stránky nebo v případě, že je pro existující stránku vyžadováno jiné rozvržení.</p><p>**Kde je upravováno:** rozvržení jsou vytvořena v editoru rozvržení. K vytvoření nebo úpravě není nutné žádný kód.</p> |
| [Instance stránky](modify-existing-page.md) | <p>**Definice:** instance stránky definují finální obsah lokalizovaný dle konkrétní stránky pro jednu stránku. Tento obsah je odvozen z hodnot vlastností modulu.</p><p>**Kde je vybráno:** stránky jsou vybrány při přiřazení adres URL.</p><p>**Kde je upravováno:** stránky jsou vytvořeny v editoru stránek. K vytvoření nebo úpravě není nutné žádný kód.</p> |
| [Motiv](select-site-theme.md) | <p>**Definice:** motivy definují kaskádovou šablonu stylů (CSS) a určují vzhled a chování modulů, které jsou vykresleny na stránce.</p><p>**Kde je vybráno:** po odeslání motivu na web pomocí Microsoft Dynamics Lifecycle Services (LCS) je možné jej vybrat jako vlastnost modulu kontejneru stránky.</p><p>**Kde je upravováno:** motivy jsou aktuálně vytvářeny a upravovány pomocí sady SDK. Poté jsou odeslány na váš web pomocí LCS.</p> |
| [Fragment](work-with-fragments.md) | <p>**Definice:** fragmenty jsou plně konfigurované moduly, které mají lokalizovaný obsah, který lze opakovaně použít a centrálně aktualizovat přes více stránek. Fragment, který je vytvořen z modulu záhlaví, lze například použít ve všech šablonách a na všech stránkách na celém webu a centrálně aktualizovat na jednom místě.</p><p>**Kde je vybráno:** fragmenty lze vybrat všude, kde lze vybrat moduly. Mohou být nahrazeny modulem, který pomůže zvýšit účinnost pomocí opakovaně použitelného a centralizovaného vytváření.</p><p>**Kde je upravováno:** fragmenty jsou vytvořeny v editoru fragmentů. K vytvoření nebo úpravě není nutné žádný kód.</p> |
| [URL](create-page-URL.md) | <p>**Definice:** adresy URL jsou adresy, které odkazují na webové stránky nebo jiné adresy URL.</p><p>**Kde je vybráno:** adresy URL jsou, pokud jsou požadovány odkazy mezi stránkami.</p><p>**Kde je upravováno:** adresy URL se upravují v editoru adres URL. K vytvoření nebo úpravě není nutné žádný kód.</p> |
| Majetek | <p>**Definice:** aktiva jsou binární soubory, které mají příponu jako .jpg, .docx, .pdf nebo .mpg.</p><p>**Kde je vybráno:** jsou vybrány položky jako vlastnosti modulu pro moduly, které je vyžadují.</p><p>**Kde je upraveno:** aktiva se nahrají a přidružená metadata se upravují ve správci aktiv.</p> |

## <a name="additional-resources"></a>Další zdroje

[Způsoby přidání obsahu](add-manage-content.md)

[Stavy dokumentu a životního cyklu](document-states-overview.md)

[Práce s publikovacími skupinami](publish-groups.md)

[Povolení a používání sdílení napříč kanály](cross-channel-sharing.md)

[Práce s moduly](work-with-modules.md)

[Práce s fragmenty](work-with-fragments.md)

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Přizpůsobení navigace na webu](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
