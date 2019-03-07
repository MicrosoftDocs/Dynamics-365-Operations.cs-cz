---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (31. října 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c5acd09e25ecd5fefa637342f83d0ee0f1891402
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303590"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (31. října 2018)

[!include [banner](includes/banner.md)]

**Sestavení 8.1.2031**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.

## <a name="create-links-from-talent-to-finance-and-operations"></a>Vytvoření propojení z aplikace Talent do aplikace Finance and Operations
Tato nová navigační funkce vám umožní propojit se z aplikace Talent do aplikace Finance and Operations, což vám umožní přímý přechod na stránky aplikace Finance and Operations. Po nastavení propojení můžete zadat název a skupinu propojení, kde se má propojení objevit v aplikaci Talent a cílovou stránku, která se otevře v aplikaci Finance and Operations.

#### <a name="coming-soon"></a>Již brzy
Kontext pole bude přidán později, aby umožnil přímý přechod na odpovídající záznamy v aplikaci Finance and Operations. Například můžete použít **Odkaz na pole** pro poskytnutí kontextu k přímému přechodu na konkrétního zaměstnance nebo pozici v aplikaci Finance and Operations.

### <a name="configure-target-systems"></a>Konfigurace cílových systémů

V aplikaci Talent mohou definovat správci systému propojení, která se zobrazí, prostřednictvím pracovního prostoru Správa systému. Součástí konfigurace je prostředí Finance and Operations, do kterého chcete přejít jako do cíle propojení. Toho dosáhnete přiřazením názvu cílovému systému a zadáním URL adresy prostředí Finance and Operations. Zde je příklad URL adresy Finance and Operations, kterou můžete zadat: https://devax00124aos.cloud.test.dynamics.com/. Po nakonfigurování cílových systémů můžete nadefinovat svá propojení.

### <a name="configure-links"></a>Konfigurovat odkaz

Každé propojení, které je vytvořeno, má definovány následující informace.

- Propojení – Název propojení, používaný pouze k identifikaci.

- Povolit toto propojení - Nastavte tuto možnost na **Ano**, pokud chcete zobrazit toto propojení pro uživatele aplikace Talent.

- Zobrazovaný název – Definujte název, který se zobrazí jako propojení do aplikace Finance and Operations. Tato data nejsou momentálně přeložena.

- Odkaz na místo zobrazení ve formuláři - Vyberte, na které stránce se má zobrazit propojení.

- Skupina - Skupiny nejsou vyžadovány, ale pokud chcete uspořádat svá propojení pomocí skupin, vyberte existující skupinu, nebo vytvořte novou pomocí pole **Skupina**.

- Cílový systém - Vyberte cílový systém, který byl vytvořen pomocí možnosti **Konfigurace cílového systému**. Bude se jednat o prostředí Finance and Operations, které bude použito při navigaci pomocí propojení.

- Použít aktuální společnosti uživatele – Vyberte **Ano**, budete-li chtít používat kontext aktuální společnosti uživatele při navigaci do Finance and Operations. Pokud zvolíte **Ne**, můžete vybrat společnost, která má být použita.

- Cílová položka nabídky- Zadejte položku nabídky z Finance and Operation, kterou má používat propojení při navigaci. K dispozici jsou položky nabídky, ke kterým můžete přímo navigovat. Chcete-li vyhledat požadovanou položku nabídky, otevřete Finance and Operations a otevřete stránku, která je cílem navigace. Zkopírujte položku nabídky z adresy URL. Například pokud chcete, aby vás odkaz navedl na seznam zaměstnanců v aplikaci Finance and Operations, zadejte hodnotu, které se objeví v URL adrese za „&mi“. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Položka nabídky pro navigaci na stránku se seznamem zaměstnanců v tomto příkladu je: HcmWorkerListPage_Employees.

- Odkaz na zdroj dat – Vyberte zdroj dat, na která se odkaz odkazuje. Nejběžnější zdroje, jako je například **Pracovník** a **Pozice**, jsou k dispozici.

- Odkaz na pole - (připravuje se) Tento výběr pole umožní přímou navigaci z jednoho záznamu v aplikaci Talent do jednoho záznamu v aplikaci Finance and Operations.

### <a name="access-to-links"></a>Přístup k odkazům

Správci systému uvidí nově vytvořené odkazy na definovaných stránkách, i když je možnost **Povolit tento odkaz** nastavena na **Ne**. To lze použít k testování odkazů předtím, než budou vystaveny k použití pro jiné zaměstnance. Všechny ostatní role uvidí jen konfigurované odkazy poté, co bude možnost **Povolit teto odkaz** nastavena na **Ano**. Zaměstnanci, kteří mají přístup ke stránkám, na kterých jsou odkazy k dispozici, budou mít přístup k odkazům.

Uživatelé také mají bezpečnostní oprávnění v rámci aplikace Finance and Operations definované pro přístup ke stránkám v aplikaci Finance and Operations. Pokud ne, zobrazí se při použití odkazu dialogové okno zabezpečení.


## <a name="other-changesfixes"></a>Další změny/opravy

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Pozice s budoucím počátečním datem nelze přiřadit k novému zaměstnanci

Byly provedeny změny, které umožní přiřazení zaměstnanců k pozicím s budoucím datem. Pozice, které mají počáteční datum v budoucnosti, lze vybrat, a přiřazení zaměstnance bude provedeno při uložení nebo dokončení workflow (pokud je workflow povoleno).

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Nový zaměstnanec nemůže být přiřazen k existující pozici

Byly provedeny změny, aby mohl být nový zaměstnanec přiřazen k existujícím pozicím.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Datum služebního věku/Umístění pracoviště zmizí, když je počáteční datum zaměstnání v minulosti a záznam je ukládán.

Byly provedeny změny, aby byla opravena viditelnost položek **Datum služebního věku** a **Umístění pracoviště** při ukládání bývalých zaměstnanců.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Nelze zadat data pro budoucí zaměstnání na stránce pracovníka

Na hlavní stránce pracovníka byla zakázána data zaměstnání pro budoucí zaměstnání. Data zaměstnání lze zadat pomocí stránek **Správce dat**. Další změny budou provedeny v příštích verzích, aby bylo možné zadávat údaje o zaměstnancích během procesu workflowu.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>Přidání ValidFrom a ValidTo do HcmPersonalContactPersonEntity

Enitita Data Management Framework (DMF) s názvem HcmPersonalContactPersonEntity byla aktualizována tak, aby zahrnovala data „platné od“ a „platné do“ pro povolení určitých scénářů integrace výhod. 

## <a name="known-issue"></a>Známý problém
- **Problém**: Při přidání nové přílohy k pracovníkovi jsou tlačítka **Nová** a **Upravit** zobrazena šedě. 
- **Řešení:** Než otevřete stránku přílohy, ujistěte se, že jsou zavřena okna s fakty na stránce **Pracovník**. Jsou-li okna s fakty uzavřena při načítání stránky **Pracovník**, budou tlačítka přílohy k dispozici. (Tento problém bude opraven v další aktualizaci Platform Update.)
