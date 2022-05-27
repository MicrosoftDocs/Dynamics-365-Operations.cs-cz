---
title: Sloučení infrastruktury Dynamics 365 Human Resources – aktualizace verze 10.0.25
description: Toto téma poskytuje informace o Microsoft Dynamics 365 Human Resources verze 10.0.25, které přináší první vlnu schopností při sloučení infrastruktury.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bf7ce43785e3ef485074f2b0294caea381f8f726
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688085"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Sloučení infrastruktury Dynamics 365 Human Resources – aktualizace verze 10.0.25

Verze 10.0.25 přináší první vlnu schopností při sloučení infrastruktury. Během sloučení infrastruktury bude Microsoft Dynamics 365 Human Resources sloučeno s infrastrukturou Finance and Operations. Nadále však bude licencována jako nezávislá aplikace, jako je Dynamics 365 Finance a Dynamics 365 Supply Chain Management. Další informace o sloučení infrastruktury viz [Časté dotazy o sloučení infrastruktury Dynamics 365 Human Resources](../human-resources/hr-infrastructure-merge-faq.md).

Sloučení poskytne uživatelům Human Resources konzistenci následujícími způsoby:

- [Správa prostředí a integrace jsou konzistentní mezi finančními a provozními aplikacemi a aplikacemi Human Resources.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Spravujte prostředí v Microsoft Dynamics Lifecycle Services, Hledání problémů a Regression Suite Automation Tool.
    - Existuje jednotná kódová základna, kde jsou nové funkce pro Human Resources uvolněny jako součást pravidelného procesu aktualizace jedné verze.
    - Způsob, jakým jsou upgrady, aktualizace a opravy hotfix aplikovány na prostředí, je konzistentní.

- [Možnosti rozšiřitelnosti jsou vylepšeny.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options)

    - Můžete pokračovat v používání nástrojů Microsoft Power Platform k rozšíření podle potřeby.
    - Funkčnost můžete rozšířit prostřednictvím formulářů, tabulek, metod a rozhraní API.
    - Můžete vytvářet a rozšiřovat entity.

    Další informace o možnostech rozšíření, které jsou k dispozici, viz [Přehled rozšiřitelnosti v Dynamics 365](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Vytvoření jedné sady funkcí Human Resources v Dynamics 365.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/create-one-set-human-resources-capabilities-within-dynamics-365)

    Ve verzi 10.0.25 byly v infrastruktuře Finance a Operations zpřístupněny funkční schopnosti, které existovaly pouze v Human Resources. Aby zákazníci mohli využívat výhody těchto schopností v prostředí Finance and Operations, musí být ve správě funkcí povoleny následující funkce Human Resources.

    | Název funkce | Přehled | Stav uvolnění | 
    |--------------|----------|----------------| 
    | Výpočet odpracovaných let | Možnost nastavení vám umožní vybrat datum, které se použije pro výpočet **Roky služby**. | Obecně dostupné | 
    | Rozšíření prostředí pracovního postupu | Tato funkce poskytuje vylepšené uživatelské prostředí pro odesílání a schvalování pracovních postupů. | Obecně dostupné | 
    | Tisknout kontroly výkonu | Recenze výkonu si můžete vytisknout ve formátu PDF. | Obecně dostupné | 
    | Vlastní odkazy v **samoobsluze pro manažery** | Můžete vytvořit vlastní odkazy, které se zobrazí v části **Související odkazy** **samoobsluhy pro manažery**. | Obecně dostupné | 
    | Zobrazit kompenzaci mezi společnostmi | Uživatelé si mohou prohlížet kompenzační plány v **samoobsluze pro manažery** napříč všemi právnickými osobami, aniž by bylo nutné měnit společnosti. | Obecně dostupné | 
    | Konfigurace úrovní kompenzací podle práce\*&dagger; | Práce nyní podporují více úrovní kompenzací. | Náhled | 
    | Správa úkolů\* | Můžete vytvořit kontrolní seznamy a úkoly pro proces onboardingu, zrušení zprovoznění a přechodu. | Náhled | 
    | Zjednodušené zadávání zaměstnance | Tato funkce poskytuje aktualizované uživatelské prostředí na stávající stránce **Pracovník**. | Náhled | 
    | Vylepšení uživatelského prostředí Human Resources | Viz tabulka v další části.  | Náhled | 

\* Tato funkce musí být zapnuta před funkcí **Vylepšení uživatelského rozhraní Human Resources**.

&dagger; Tuto funkci nelze po zapnutí vypnout.

## <a name="human-resource-user-experience-enhancements"></a>Vylepšení uživatelského rozhraní Human Resources

| Název funkce | Přehled | 
|--------------|----------| 
| Odstranit zaměstnání | Pracovní poměr zaměstnance můžete smazat. | 
| Skupiny pracovních míst | Můžete sledovat skupinu pracovních míst, která zahrnují podobnou práci a která vyžadují podobné školení, dovednosti, znalosti a odborné znalosti. | 
| Další pole zaměstnání | Byla přidána následující pole: **Kategorie zaměstnání**, **Typ zaměstnání** a **Stav zaměstnání**. | 
| Stránka **Pracovníci bez zaměstnání** | Stránka zobrazuje seznam pracovníků, kteří nemají záznam o zaměstnání. | 
| Aktualizace uživatelského prostředí dimenze pozice | K dispozici je vylepšené uživatelské rozhraní pro přiřazování dimenzí pozic podle právnické osoby. | 
| Změny adresy v pracovním prostoru **Správa zaměstnanců** | Tato funkce poskytuje počet všech změn adres, ke kterým došlo během zadaného počtu dnů podle definice na stránce **Parametry Human Resources**. | 
| Vypršení platnosti záznamů v pracovním prostoru **Správa zaměstnanců** | Tato funkce poskytuje seznam položek, kterým vypršela nebo vyprší platnost certifikátů, identifikací, zkušebních lhůt, screeningů nebo testů. | 
| Stránka **Ověření hierarchie pozic** | Provádí se kontrola kruhových referencí v hierarchii linie pozic. | 
| Informace o mzdách pro konkrétní zemi | Další mzdová pole jsou k dispozici na stránce **Zaměstnání pracovníka** v závislosti na zemi nebo regionu právnické osoby, kde jsou pracovníci zaměstnáni. | 
| Vylepšení hlášení dodržování předpisů | Další možnosti hlášení jsou k dispozici pro EEO-1, Vets 4212 a OSHA300a. | 
| Aktualizace pracovního prostoru **Správa zaměstnanců** | Byly provedeny aktualizace za účelem sledování změn adres a záznamů, jejichž platnost končí. Nové karty navíc obsahují seznam akcí pracovníka a pozice. | 
