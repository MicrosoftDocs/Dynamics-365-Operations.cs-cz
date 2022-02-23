---
title: Rozšířené vyhledávání formátu elektronického výkaznictví
description: Toto téma popisuje, jak lze nastavit odkaz formátu elektronického výkaznictví ve vyhledávání formátu elektronického výkaznictví v případě, že je v globálním úložišti uložen požadovaný formát.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7c6cb99a6c5cc6fb92ce52041296af2d0c6722e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679479"
---
# <a name="allow-users-to-set-up-an-er-format-reference-inquiring-a-format-from-the-global-repository"></a>Umožňuje uživatelům nastavit odkaz formátu elektronického výkaznictví s dotazem na formát z globálního úložiště.

[!include [banner](../includes/banner.md)]

Můžete použít rámec [elektronického výkaznictví ](general-electronic-reporting.md) pro konfiguraci [formátů](general-electronic-reporting.md#FormatComponentOutbound) odchozích dokumentů v souladu s právními požadavky různých zemí/oblastí. Pomocí rámce elektronického výkaznictví můžete také konfigurovat [formáty](general-electronic-reporting.md#FormatComponentInbound) pro analýzu příchozích dokumentů a použít informace z těchto dokumentů k připojení nebo aktualizaci dat aplikace. Každý z těchto formátů lze použít v instanci Dynamics 365 Finance pro zpracování příchozích nebo odchozích obchodních dokumentů jako součást určitého obchodního procesu.

Obvykle je nutné určit, který formát elektronického výkaznictví je nutné použít v určitém obchodním procesu. Chcete-li to provést, vyberte ve vyhledávacím poli, které je nakonfigurováno jako součást specifických parametrů obchodního procesu, jeden formát elektronického výkaznictví. Tato vyhledávací pole jsou obvykle implementována pomocí vhodného rozhraní API rámce elektronického výkaznictví. Další informace naleznete v tématu [Rozhraní API rámce elektronického výkaznictví - kód pro zobrazení vyhledávání mapování formátu](er-apis-app73.md#code-to-display-a-format-mapping-lookup).

Pokud například konfigurujete [parametry zahraničního obchodu](https://docs.microsoft.com/dynamics365/finance/localizations/emea-intrastat#set-up-foreign-trade-parameters), je nutné nastavit odkazy na jednotlivé formáty elektronického výkaznictví, které budou použity ke generování prohlášení Intrastat a sestavy řízení prohlášení Intrastat. Snímky obrazovky níže ukazují, jak vypadají vyhledávací pole formátů elektronického výkaznictví na stránce **Parametry zahraničního obchodu**.

Pokud aktuální instance aplikace Finance neobsahuje žádné formáty elektronického výkaznictví související s obchodním procesem systému Intrastat, bude toto vyhledávací pole prázdné.

[![Stránka Parametry zahraničního obchodu](./media/ER-ExtLookup-Lookup1.gif)](./media/ER-ExtLookup-Lookup1.gif)

Pokud aktuální instance aplikace Finance neobsahuje žádné formáty elektronického výkaznictví související s obchodním procesem systému Intrastat, toto vyhledávací pole nabídne formáty elektronického výkaznictví.

[![Stránka Parametry zahraničního obchodu](./media/ER-ExtLookup-Lookup2.png)](./media/ER-ExtLookup-Lookup2.png)

Toto vyhledávání nabízí pouze formáty elektronického výkaznictví, které již byly importovány do aktuální instance Finance. Chcete-li [importovat](./tasks/er-import-configuration-lifecycle-services.md) řešení elektronického výkaznictví do aktuální instance Finance, musíte mít oprávnění ke spuštění příslušné funkce rámce elektronického výkaznictví, která podporuje [životní cyklus](general-electronic-reporting-manage-configuration-lifecycle.md) řešení elektronického výkaznictví obsahující formáty elektronického výkaznictví.

Při spuštění verze Finance 10.0.9 (vydání z dubna 2020) bylo rozšířeno uživatelské rozhraní vyhledávání formátu elektronického výkaznictví, které je implementováno pomocí rozhraní API rámce elektronického výkaznictví. Stále je možné vybrat existující formáty elektronického výkaznictví, které jsou na záložce s náhledem **Vybrat konfiguraci formátu**. Kromě toho nabízí rozšířené vyhledávání novou možnost vyhledávání v globálním úložišti za účelem vyhledání konkrétních formátů elektronického výkaznictví. Všechny formáty elektronického výkaznictví globálního úložiště jsou nabízeny na záložce s náhledem **Import z globálního úložiště**.

[![Stránka Parametry zahraničního obchodu](./media/ER-ExtLookup-Lookup3.png)](./media/ER-ExtLookup-Lookup3.png)

Podobně jako u záložky s náhledem **Vybrat formát konfigurace** zobrazuje záložka s náhledem **Import z globálního úložiště** zobrazuje pouze formáty elektronického výkaznictví, které se vztahují k obchodnímu procesu, pro který je vybrán formát elektronického výkaznictví v tomto vyhledávacím poli. V tomto příkladu se jedná o generování prohlášení systému Intrastat. Formát elektronického výkaznictví je použitelný pro společnost, k níž je uživatel aktuálně přihlášen, v závislosti na kontextu země společnosti.

Při výběru formátu elektronického výkaznictví na záložce s náhledem **Import z globálního úložiště** je vybraná [konfigurace](general-electronic-reporting.md#Configuration) formátu elektronického výkaznictví importována z globálního úložiště do aktuální instance Finance.

[![Stránka Parametry zahraničního obchodu](./media/ER-ExtLookup-FormatImport.png)](./media/ER-ExtLookup-FormatImport.png)

Po úspěšném dokončení importu bude v tomto vyhledávacím poli uložen odkaz na importovaný formát elektronického výkaznictví. Při prvním přístupu ke globálnímu úložišti je nutné použít poskytnutý odkaz pro registraci k [Regulatory Configuration Service](https://aka.ms/rcs), která se používá pro správu přístupu ke globálnímu úložišti.

[![Stránka Parametry zahraničního obchodu](./media/ER-ExtLookup-RepoSignUp.png)](./media/ER-ExtLookup-RepoSignUp.png)

Ve výchozím nastavení záložka s náhledem **Import z globálního úložiště** zobrazí seznam formátů elektronického výkaznictví z dočasného úložiště, které je automaticky vytvořeno na základě obsahu globálního úložiště pro zlepšení výkonu. K tomu dojde při prvním otevření záložky s náhledem **Import globálního úložiště**, což může trvat několik sekund.

Pokud na záložce s náhledem **Import z globálního úložiště** nevidíte požadovaný formát elektronického výkaznictví, ale jste si jisti, že tento formát elektronického výkaznictví je uložen v globálním úložišti, vyberte možnost **Synchronizovat**. Tato možnost aktualizuje dočasné úložiště a synchronizuje ho s aktuálním obsahem globálního úložiště.

## <a name="feature-activation"></a>Aktivace funkce

Dostupnost této funkce je řízena funkcí **Rozšířené vyhledávání konfigurací formátu elektronického výkaznictví, které umožňují dotázat globální úložiště** ve **správě funkcí**. Tato funkce je povolena ve výchozím nastavení.

[![Stránka Správa funkcí](./media/ER-ExtLookup-FeatureMngt.png)](./media/ER-ExtLookup-FeatureMngt.png)

## <a name="security-considerations"></a>Na co brát ohled při zabezpečení

Oprávnění **Spravovat úložiště konfigurací** (**ERMaintainSolutionRepositories**) řídí přístup ke globálnímu úložišti pro uživatele, který otevírá vyhledávání formátu elektronického výkaznictví s povolenou záložkou s náhledem **Import z globálního úložiště**. Chcete-li uživatelům umožnit přístup k obsahu globálního úložiště z vyhledávání formátu elektronického výkaznictví, je nutné změnit nastavení zabezpečení udělením oprávnění **ERMaintainSolutionRepositories** uživatelům buď přímo, nebo pomocí již přiřazených rolí a funkčních oprávnění.

Následující snímek obrazovky ukazuje, jak může být toto oprávnění uděleno uživatelům, kteří jsou přiřazeni k roli **Účetní**. Tato role umožňuje uživatelům konfigurovat parametry zahraničního obchodu a nastavit odkazy na formáty elektronického výkaznictví v polích **Mapování formátu souborů** a **Mapování formátu sestavy** na stránce **Parametry zahraničního obchodu**.

[![Stránka Konfigurace zabezpečení](./media/ER-ExtLookup-SecuritySetting.png)](./media/ER-ExtLookup-SecuritySetting.png)

## <a name="limitations"></a>Omezení

Přístup k globálnímu úložišti ve vyhledávání formátu elektronického výkaznictví je v současné době podporován pouze pro výběr formátů elektronického výkaznictví, které se používají ke generování odchozích dokumentů.

## <a name="frequently-asked-questions"></a>Časté dotazy

### <a name="why-cant-i-access-the-global-repository-from-the-er-format-lookup"></a>Proč nelze získat přístup ke globálnímu úložišti z vyhledávání formátu elektronického výkaznictví?

Pokud jste povolili funkci **Rozšířené vyhledávání konfigurací formátu elektronického výkaznictví, které umožňují dotázat globální úložiště** na stránce **Správa funkcí**, ale uživatelé nevidí formáty elektronického výkaznictví na záložce s náhledem **Import z globálního úložiště** a možnost **Synchronizovat** je sice viditelná, ale zakázaná, ujistěte se, že oprávnění **Udržovat úložiště konfigurace** (**ERMaintainSolutionRepositories**) bylo uděleno uživateli. Chcete-li toto oprávnění obdržet, obraťte se na správce systému.

## <a name="additional-resources"></a>Další zdroje

- [Přehled elektronického výkaznictví](general-electronic-reporting.md)
- [API rozhraní architektury elektronického výkaznictví](er-apis-app73.md)
- [Správa životního cyklu konfigurace elektronického vykazování](general-electronic-reporting-manage-configuration-lifecycle.md)
