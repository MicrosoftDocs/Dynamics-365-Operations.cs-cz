---
title: Zřízení Human Resources ve finanční a provozní infrastruktuře
description: Tento článek vysvětluje proces zřizování nového produkčního prostředí pro Microsoft Dynamics 365 Human Resources ve finanční a provozní infrastruktuře.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2fd8176d16178ecc4ba667e5937f2cec2e0af2c3
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/03/2022
ms.locfileid: "9221585"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Zřízení Human Resources ve finanční a provozní infrastruktuře

_**Týká se:** Zřízení Human Resources v infrastruktuře finanční a provozní aplikace_ 

> [!NOTE]
> Od července 2022 nebude možné v samostatné infrastruktuře Human Resources zřizovat nová prostředí Human Resources a projekty Microsoft Dynamics Lifecycle Services (LCS) na něm nelze vytvářet. Zákazníci mohou nasadit prostředí Human Resources na finanční a provozní infrastrukturu.

Tento článek vysvětluje proces zřizování nového produkčního prostředí pro Microsoft Dynamics 365 Human Resources ve finanční a provozní infrastruktuře.

## <a name="prerequisites"></a>Předpoklady

Aby bylo možné zřídit nové prostředí, musí být zavedeny následující předpoklady:

- Zakoupili jste si aplikaci Human Resources prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). Pokud máte existující licenci pro Dynamics 365, která obsahuje servisní plán aplikace Human Resources, a nedaří se vám provést kroky uvedené v tomto článku, kontaktujte podporu.
- Globální správce se přihlásil do služby [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) a vytvořil nový projekt financí a provozu.

## <a name="provision-a-human-resources-trial-environment"></a>Zřídit zkušební prostředí Human Resources

> [!NOTE]
> Od dubna 2022 nebudou zkušební prostředí Human Resources dostupná v samostatné aplikaci. Potenciální zákazníci, kteří mají zájem o vyhodnocení schopností Human Resources v rámci finančních a provozních aplikací, tak mohou učinit pomocí bezplatné 30denní zkušební verze spolu s ukázkovými daty. Dynamics 365 Finance bude zahrnovat funkce Human Resources přenesené do infrastruktury Finance sloučením samostatné aplikace. Více informací viz [Sloučení nabídek HR přináší zákazníkům funkce](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Další informace o zkušebních verzích Dynamics 365 Finance naleznete v [průvodci krok za krokem](../fin-ops-core/fin-ops/get-started/before-you-buy.md).

## <a name="plan-human-resources-environments"></a>Plánování prostředí Human Resources

Než vytvoříte své první prostředí Human Resources, měli byste pečlivě naplánovat potřeby prostředí pro váš projekt. Základní předplatné Human Resources zahrnuje dvě prostředí: produkční prostředí a výchozí prostředí standardní zkoušky přijatelnosti (sandbox). V závislosti na složitosti vašeho projektu máte možnost zakoupit další prostředí pro podporu projektových aktivit.

Zde jsou doporučení pro další volitelná prostředí:

- **Migrace dat** – Aktivity migrace dat umožňují vaše prostředí karantény použít pro účely testování v celém projektu. Mít další prostředí umožňuje, aby aktivity migrace dat pokračovaly, zatímco aktivity testování a konfigurace probíhají současně v jiném prostředí.
- **Integrace** – Konfigurace a testování integrací, které by mohly zahrnovat nativní integrace nebo vlastní integrace, jako jsou integrace pro mzdy, systémy sledování žadatelů nebo systémy a poskytovatele výhod.
- **Školení** – Abyste mohli své zaměstnance vyškolit v používání nového systému, možná budete potřebovat samostatné prostředí, které je nakonfigurováno se sadou tréninkových dat. 
- **Vícefázový projekt** – Možná budete potřebovat další prostředí pro podporu konfigurace, migrace dat, testování nebo jiných aktivit ve fázi projektu, která je plánována po počátečním uvedení projektu do provozu.
- **Vývoj** – Ve finanční a provozní infrastruktuře nyní můžete rozšiřovat řešení a vyvíjet svá vlastní přizpůsobení. Každý vývojář musí používat své vlastní vývojové prostředí. Další informace viz [Nasazení a přístup k vývojovým prostředím](../fin-ops-core/dev-itpro/dev-tools/access-instances.md).
- **GOLD** – Pro nová nasazení je běžnou praxí použití samostatného prostředí GOLD, které je udržováno v původním stavu pro konfiguraci a migraci dat. Toto prostředí lze použít po celou dobu implementace k obnovení jiných prostředí. Bude použit k vytvoření nového produkčního prostředí, které má základní konfiguraci a migraci dat. Produkční prostředí nemůžete nasadit na finanční a provozní infrastrukturu, dokud nedokončíte proces připravenosti ke spuštění. Další informace naleznete v tématu [Příprava na spuštění](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Při návrhu vašich prostředí doporučujeme následující přístup:
>
> - Použijte své výchozí prostředí standardního testu přijatelnost (dříve Sandbox) nebo jiné prostředí k provedení simulovaného přechodu před spuštěním.
> - Ponechte si podrobný kontrolní seznam pro vystřihování, který zahrnuje každý z datových balíčků potřebných k migraci konečných dat do produkčního prostředí během zastávky. Toto doporučení je zvláště důležité, pokud nemáte samostatné prostředí GOLD pro ukládání konfigurací.
> - Použijte své výchozí prostředí standardního testu přijatelnost (dříve Sandbox) nebo jiné prostředí úrovně 2 nebo vyšší jako prostředí TEST v celém projektu. Pokud potřebujete další prostředí, může si je vaše organizace za příplatek zakoupit.

## <a name="create-an-lcs-project"></a>Vytvoření LCS projektu

Pokud chcete použít ke správě svého prostředí aplikace Human Resources službu LCS, musíte nejprve vytvořit LCS projekt. Pokud migrujete prostředí Human Resources do finanční a provozní infrastruktury, musíte vytvořit nový projekt LCS pro finanční a provozní aplikace. Pokud již máte projekt LCS pro jiné finanční a provozní aplikace, můžete aktivovat funkce Human Resources v pracovním prostoru **Správa funkcí**. Další informace naleznete v tématu [Přehled správy funkcí](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Když se nový zákazník zaregistruje do Human Resources, předplatné zahrnuje pracovní prostor projektu implementace. Poté, co si zákazník službu aktivuje, musí se správce tenanta přihlásit na <https://lcs.dynamics.com> pomocí účtu tenanta. Pro organizaci se automaticky vytvoří pracovní prostor projektu. Další informace získáte v tématu [Lifecycle Services (LCS) pro zákazníky finančních a provozních aplikací](../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md).

> [!NOTE]
> Aby bylo zajištěno úspěšné zřízení, účet, který používáte k zřízení prostředí Human Resources, musí být přiřazen buď roli **Správce systému**, nebo **Přizpůsobení systému** v prostředí Power Apps spojeném s prostředím Human Resources. Další informace o přiřazení rolí zabezpečení uživatelům v Microsoft Power Platform získáte v části [Konfigurace zabezpečení uživatele u zdrojů](/power-platform/admin/database-security).

Než budete moci začít nasazovat prostředí, musíte dokončit proces onboardingu projektu LCS. Další informace naleznete v tématu [Onboarding projektu](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md). Další informace o tom, jak používat LCS, viz [Uživatelská příručka Lifecycle Services (LCS).](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md).

## <a name="deploy-human-resources-environments"></a>Nasazení prostředí Human Resources

Nasazení finančních a provozních aplikací, včetně Human Resources, v cloudu vyžaduje, abyste rozuměli prostředí a předplatnému, do kterého nasazujete, kdo může provádět jaké úkoly a jaká data a přizpůsobení musíte spravovat. Při nasazování nových prostředí doporučujeme místo pojmenovaného uživatele použít účet služby. Další informace o tom, jak nasadit prostředí ve finanční a provozní infrastruktuře, viz [Přehled cloudového nasazení](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Chcete-li nasadit produkční prostředí pro Human Resources na finanční a provozní infrastrukturu, musíte provést proces připravenosti ke spuštění. Další informace naleznete v tématu [Příprava na spuštění](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md). Tento proces zahrnuje odhad předplatného v LCS. Další informace naleznete v tématu [Nástroj pro posouzení předplatného](../fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator.md).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Integrace Microsoft Power Platform s Human Resources

Microsoft Power Platform poskytuje sadu funkcí pro aplikace Dynamics 365 prostřednictvím centra pro správu Power Platform. Pomocí Microsoft Power Platform lze integrovat a rozšířit použití dat Human Resources. Informace o tom, jak integrovat lidské zdroje s Microsoft Power Platform, viz [Integrace Microsoft Power Platform s finančními a provozními aplikacemi](../fin-ops-core/dev-itpro/power-platform/overview.md).

## <a name="supported-geographies"></a>Podporované zeměpisné oblasti

Informace o jazycích a zeměpisných oblastech, které jsou podporovány pro Human Resources, naleznete v části [Globální od návrhu: zjistěte více o podporovaných zemích a jazycích](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Zřízení přístupu k prostředí

Ve výchozím nastavení má k prostředí přístup globální správce, který ho vytvořil. Dalším uživatelům aplikace musíte explicitně udělit přístup. Musíte přidat uživatele a přiřadit jim příslušné role v prostředí Human Resources. Další informace naleznete v tématu [Vytvoření nových uživatelů](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) a [Přiřazení uživatelů k rolím zabezpečení](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Další prostředky
Další informace o tom, jak používat a spravovat projekty v LCS v infrastruktuře finančních a provozních aplikací, můžete získat pomocí následujících zdrojů:

- [Zdroje pro Lifecycle Services](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Uživatelská příručka Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Přehled samoobslužného nasazení](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Úvodní stránka operace přesunu databáze](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
