---
title: Migrace zákazníků Dynamics 365 Human Resources do finanční a provozní infrastruktury
description: Tento článek popisuje migraci zákazníků Microsoft Dynamics 365 Human Resources do finanční a provozní infrastruktury.
author: twheeloc
ms.date: 10/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63b08a8493702cf319aa078ef6aa787e2094be87
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733435"
---
# <a name="dynamics-365-human-resources-customer-migration"></a>Migrace zákazníků Dynamics 365 Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

Migrace zákazníků je migrování metodou "lift-and-shift" (přesunutí) databáze zákazníků do finanční a provozní infrastruktury. Používají se k ní nástroje pro automatizovanou migraci. Výsledkem je nové finanční a provozní prostředí, které využívá databázi lidských zdrojů zákazníka.

## <a name="prerequisites"></a>Předpoklady

### <a name="user-access-and-permissions"></a>Přístup a oprávnění uživatelů

- Uživatel Microsoft Dynamics Lifecycle Services by měl mít roli **Správce organizace**.
- Uživatel by měl být schopen [vytvářet projekty Azure DevOps](/azure/devops/organizations/projects/create-project) nebo používat existující projekty Azure DevOps.
- Uživatel by měl mít přístup k [vytvoření tokenu zabezpečení osobního přístupu Azure DevOps](/azure/devops/organizations/accounts/use-personal-access-tokens-to-authenticate) nebo by měl mít token, který je k dispozici k použití.

### <a name="dataverse-environment-backup-sandbox"></a>Záloha prostředí Dataverse (Sandbox)

1. Volitelné, ale doporučené: Doporučujeme: Obnovte stávající sandboxové prostředí Human Resources pomocí kopie provozního prostředí Human Resources.
2. [Vytvořte nové prostředí Dataverse](/power-platform/admin/create-environment#create-an-environment-with-a-database) pomocí centra pro správu Power Platform.

    > [!NOTE]
    > Když přidáváte databázi, ujistěte se, že je možnost **Povolit aplikace Dynamics 365** nastavena na **Ano**.

3. [Zkopírujte existující prostředí Dataverse](/power-platform/admin/copy-environment), které je propojeno se samostatnou aplikací Human Resources, s prostředím, které jste vytvořili v předchozím kroku.

### <a name="dataverse-capacity"></a>Kapacita Dataverse

1. Použijte **souhrnnou** stránku v centru pro správu Power Platform pro ověření, že [úložiště Dataverse](/power-platform/admin/finance-operations-storage-capacity) má dostatek dostupné kapacity pro kopii prostředí.
2. Pokud není k dispozici dostatečná kapacita, použijte [pokyny, jak uvolnit úložný prostor](/power-platform/admin/free-storage-space) pro snížení celkové spotřeby. Zákazníci také mohou [přidat další kapacitu úložiště](/power-platform/admin/add-storage).

## <a name="customer-migration-process"></a>Proces migrace zákazníků

### <a name="create-a-lifecycle-services-project-for-human-resources-migration"></a>Vytvořte nový projekt Lifecycle Services pro migraci Human Resources

Prvním krokem je vytvoření nového projektu implementace financí a provozu v Lifecycle Services. Zákazník bude mít existující projekt Human Resources Lifecycle Services. Existující prostředí Human Resources bude migrováno do nového procesu implementace financí a provozu.

Chcete-li vytvořit nový projekt, postupujte následovně.

1. Přihlaste se ke službám Lifecycle Services jako globální správce nebo určený uživatel servisního účtu.
2. Na domovské stránce Lifecycle Services vyberte položku **Vytvořit/nový (+)**.
3. Vyberte finanční a provozní aplikace jako produkt.
4. V poli **Účel projektu** vyberte **Implementace**.
5. Zadejte název a popis projektu.
6. V poli **Vlastní typ projektu** vyberte **Migrace Microsoft Dynamics 365 Human Resources**.
7. Zaškrtnutím políčka odsouhlaste smluvní podmínky.
8. Vyberte **Vytvořit**.

Poté, co jste vytvořili a nasadili nový projekt Lifecycle Services, proveďte tyto kroky k jeho nastavení a konfiguraci.

1. Vyberte **Onboarding projektu** k dokončení onboardingu projektu. Další informace naleznete v tématu [Onboarding projektu](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md).

    - Vyberte stejnou oblast jako vaše aktuální prostředí. Tento výběr neovlivní migraci.
    - U starších systémů vyberte **jiný**.

2. Dokončete konfiguraci projektu V rámci tohoto kroku byste měli nakonfigurovat knihovnu SharePoint Online, Azure DevOps a připojení k Azure, pokud jsou vyžadována. Další informace naleznete v [uživatelské příručce Zdroje Lifecycle Services (LCS)](../dev-itpro/lifecycle-services/lcs-user-guide.md).

> [!NOTE]
> Zákazníci mohou využít stávající projekt Azure DevOps a související token zabezpečení osobního přístupu. Pokud je použit existující projekt, konfigurace související s projektem jsou automaticky dostupné a lze je zkontrolovat z hlediska přesnosti.

### <a name="migrate-a-human-resources-sandbox-environment"></a>Migrace sandboxového prostředí Human Resources

#### <a name="prepare-to-migrate-the-sandbox-environment"></a>Příprava na migraci sandboxového prostředí

Po vytvoření nového projektu Lifecycle Services a dokončení procesu registrace projektu jste připraveni migrovat své první prostředí. Než s tímto procesem začnete, doporučujeme obnovit sandboxové prostředí, které chcete migrovat z provozního prostředí na samostatnou infrastrukturu.

#### <a name="prepare-a-power-platform-environment"></a>Příprava prostředí Power Platform

> [!NOTE]
> Tento krok je použitelný pouze pro migraci sandboxového prostředí. Když migrujete provozní prostředí, stávající prostředí centra pro správu Power Platform, které je připojeno k provoznímu prostředí, bude přeneseno dále.

- V centru pro správu Power Platform [vytvořte prostředí Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center) k použití pro migraci sandboxu nebo vybrat existující prostředí.
- [Zkopírujte prostředí](/power-platform/admin/copy-environment) pro obnovení prostředí Power Platform, které se používá pro mapování.

#### <a name="migrate-the-sandbox-environment"></a>Migrace sandboxového prostředí

1. Přihlaste se ke službám Lifecycle Services jako globální správce nebo určený uživatel servisního účtu.

    > [!NOTE]
    > Doporučujeme používat pojmenovaný uživatelský účet. Přihlášený uživatel by měl mít roli zabezpečení **Vlastník projektu** nebo **Správce projektu** v samostatném prostředí projektu Human Resources Lifecycle Services.

2. Otevřete nově vytvořený projekt migrace lidských zdrojů.
3. Přezkoumejte a dokončete příslušné fáze metodiky migrace a zavedení projektu.
4. Na řídicím panelu projektu v podokně **Výchozí: Standardní akceptační test** vyberte **Migrovat HR**.
5. V podokně **Vyberte prostředí pro migraci** vyberte příslušný projekt Lifecycle Services a původní prostředí Human Resources (z vaší zdrojové samostatné aplikace Human Resources).
6. Povolte prostředí **Mapovat na nové prostředí Power Platform** a vyberte odpovídající prostředí Power Platform. Pak vyberte **Další**.
7. Dokončete průvodce **Nastavení nasazení (finance a provoz – sandbox)** pro potvrzení podrobností a odhlášení zákazníka a poté vyberte **Nasadit**.

Stav prostředí ukáže průběh. Stav se změní z **Načítání** přes **Nasazení** na **Nasazeno**.

> [!NOTE]
> Provozní podokno nebude k dispozici, dokud nebude dokončen kontrolní seznam připravenosti projektu na spuštění. Další informace naleznete v tématu [Příprava na spuštění](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

#### <a name="considerations-and-assumptions"></a>Úvahy a předpoklady

V projektu Lifecycle Services na v klientovi existuje sandboxové prostředí Lifecycle Services, které má následující vlastnosti:

- Sandboxové prostředí Human Resources není propojeno s existujícím sloučeným prostředím. V daném okamžiku může probíhat pouze jedna migrace pro dané prostředí Human Resources.
- Počet sandboxových prostředí, která jsou současně povolena, je založen na licencování Human Resources. Pokud bylo pro klienta zakoupeno dostatečné množství licencí, další sandboxová prostředí budou uvedena v podokně **Prostředí** projektu.
- Migrace musí být provedeny do prostředí stejného typu. Jinými slovy, lze provádět pouze migrace v rámci sandboxového nebo provozního prostředí.

    > [!NOTE]
    > Při určování stavu provozu nebo sandboxu se berou v úvahu pouze typy prostředí Human Resources. Pokud jsou prostředí nesprávně kategorizována (tj. provozní prostředí je označeno jako sandboxové nebo sandboxové prostředí je označeno jako provozní prostředí), kontaktujte podporu.

- Pokud není migrace úspěšná, zobrazí se chybová zpráva o selhání a zpřístupní se tlačítko **Odstranit**. Toto tlačítko použijte k odstranění neúspěšné migrace. Poté můžete prostředí remigrovat.

#### <a name="validate-the-sandbox-migration"></a>Ověření migrace sandboxu

Po úspěšném dokončení procesu migrace v sandboxu vytvořte podrobný plán testování k ověření a podepsání všech obchodních procesů.

Než začnete s testováním, ověřte si následující podrobnosti:

- Potvrďte, že migrované prostředí je přístupné na vygenerované adrese URL.
- Potvrďte, že uživatelé mají přístup k migrovanému sandboxu.
- Potvrďte, že prostředí Dataverse, které je přidruženo k migrovanému sandboxovému prostředí, je přístupné.
- Namátkově zkontrolujte různá data, abyste potvrdili, že jsou k dispozici nejaktuálnější data.
- Dokončete kritické obchodní procesy pro ověření.
- Potvrďte, že vaše zásady zabezpečení platí.
- Potvrďte, že se dávkové úlohy spouštějí podle očekávání.

Nebudete mít přístup ke vzdálené ploše k migrovanému sandboxu. K provádění následujících akcí pro vaše prostředí sandbox úrovně 2+ můžete použít samoobslužné funkce a nástroje:

- Přístup k [databázi Azure SQL](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-the-azure-sql-database).
- Přístup k [souborům protokolu](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-log-files).
- Použití [nástrojů perfmon](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#use-perfmon-tools).
- Vypněte/zapněte [režim údržby](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#access-self-service-logs).
- Restartujte [služby](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#restart-services).
- Nakonfigurujte [Regression suite automation tool](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md#configure-the-regression-suite-automation-tool).

Další informace viz [Časté dotazy k samoobslužnému nasazení](../fin-ops-core/dev-itpro/deployment/deploymentfaq.md).

### <a name="migrate-a-human-resources-production-environment"></a>Migrace provozního prostředí Human Resources

Po dokončení migrace a ověření sandboxového prostředí proveďte migraci provozního prostředí podle následujících kroků.

#### <a name="prerequisites"></a>Předpoklady

- Měl by být vyplněn odhad předplatného.
- Uvedení do provozu [posouzení připravenosti](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) by měla být dokončena.

#### <a name="migrate-the-production-environment"></a>Migrace provozního prostředí

1. Přihlaste se ke službám Lifecycle Services jako globální správce nebo určený uživatel servisního účtu.

    > [!NOTE]
    > Doporučujeme používat pojmenovaný uživatelský účet. Přihlášený uživatel by měl mít roli zabezpečení **Vlastník projektu** nebo **Správce projektu** v projektu Lifecycle Services.

2. Otevřete nový projekt migrace lidských zdrojů.
3. Přezkoumejte a dokončete příslušné fáze metodiky migrace a zavedení projektu.
4. Na řídicím panelu projektu v podokně **Produkce** vyberte **Migrovat HR**.
5. V podokně **Vyberte prostředí pro migraci** vyberte příslušný projekt Lifecycle Services a původní prostředí Human Resources (z vaší zdrojové samostatné aplikace Human Resources). Pak vyberte **Další**.
6. Dokončete průvodce **Nastavení nasazení (finance a provoz – sandbox)** pro potvrzení podrobností a odhlášení zákazníka a poté vyberte **Nasadit**.

Stav prostředí ukáže pokrok nasazení. Stav se změní z **Načítání** přes **Nasazení** na **Nasazeno**.

#### <a name="post-migration-considerations"></a>Předpoklady po migraci

- Použijte nejnovější [aktualizace kvality](/fin-ops-core/fin-ops/get-started/quality-updates) vašich prostředí.
- Pokud používáte [virtuální tabulky](hr-admin-integration-common-data-service-virtual-entities.md), překonfigurujte koncové body.
- Překonfigurujte integraci duálního zápisu. Vyhodnoťte, které entity musí být povoleny.
- Zvažte použití virtuálních tabulek k nahrazení duálního zápisu pro integraci.

#### <a name="dual-write-integration"></a>Integrace dvojitého zápisu

##### <a name="set-up-microsoft-power-platform-dual-write-integration"></a>Nastavení integrace duálního záznamu Microsoft Power Platform

1. přejděte do centra pro správu Power Platform a v levé navigaci vyberte **Prostředí**.
2. Vyberte dříve zkopírované/aktualizované prostředí a potvrďte, že je stav **Připraveno**.
3. Přejděte do Lifecycle Services a potvrďte, že stav projektu migrace je **Nasazeno**.
4. V migrovaném prostředí vyberte **Všechny podrobnosti** ke kontrole dalších podrobností a [nastavte aplikaci pro duální zápis](../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#set-up-dual-write-for-new-or-existing-dataverse-environments).
5. V podokně **Konfigurace aplikace s duálním zápisem** zaškrtnutím políčka vyjádřete souhlas s mapováním a synchronizací dat mezi databázemi a poté vyberte **Konfigurovat**.
6. Když vás okno se zprávou upozorní na úspěšnou konfiguraci duálního zápisu, vyberte **OK**.
7. Průběh konfigurace můžete sledovat v detailech.
8. Po dokončení konfigurace vyberte **Odkaz na prostředí Power Platform** k synchronizaci dostupných datových entit.
9. Když stav indikuje, že prostředí byla úspěšně propojena, přejděte do centra pro správu Power Platform, abyste mohli zkontrolovat a vybrat příslušné datové entity.
10. V levém podokně vyberte **Aplikace Dynamics 365 \> Zdroje**.
11. Potvrďte, že stav aplikace Human Resources s duálním zápisem je **Povoleno**.
12. Vyberte aplikaci Human Resources s duálním zápisem a poté vyberte **Instalovat**.
13. V podokně **aplikace Nainstalovat duální zápis Dynamics 365 Human Resources** vyberte vhodné prostředí pro instalaci balíčku.
14. Zaškrtnutím políčka odsouhlaste smluvní podmínky a poté vyberte **Instalovat**.
15. V prostředí aplikace Dynamics 365 bude stav **Instaluje se**, zatímco instalace probíhá. Po dokončení instalace bude aktualizován na **Instalováno**.

##### <a name="review-and-apply-a-dual-write-solution"></a>Zkontrolujte a použijte řešení s duálním zápisem

1. V novém finančním a provozním prostředí přejděte na **Správa dat \> Duální zápis**.
2. Vyberte **Použít řešení**.
3. V podokně vyberte **Dynamická instalovaná řešení**, **Mapy hlavních entit aplikací s duálním zápisem** a **Mapy Dynamics 365 Human Resources**. Pak vyberte **Použít**. Zpráva potvrzuje, že se řešení používá. Po úspěšné aplikaci řešení se zobrazí všechny dostupné mapy tabulek.
4. Prohlédněte si dostupné mapy tabulek a vyberte a spusťte integraci pomocí duálního zápisu.
5. Když poprvé spustíte integraci duálního zápisu pro mapy tabulek, vyberte zaškrtávací políčko **Počáteční synchronizace**. Pokud existuje integrace ze zdrojového prostředí Human Resources, nemusíte zaškrtávat políčko **Počáteční synchronizace** při spuštění integrace pro mapy tabulky.

#### <a name="recommended-practices"></a>Doporučené postupy

Tato část uvádí doporučení pro migraci ze samostatné infrastruktury na finanční a provozní infrastrukturu.

- Důrazně doporučujeme, abyste pracovali se svým partnerem Microsoft Dynamics, který vám pomůže s migrací vašeho prostředí Human Resources.
- Naplánujte si vhodný čas na provedení úplného uživatelského akceptačního testování (UAT) v prostředí migrovaném do sandboxu.
- Naplánujte a zdokumentujte podrobné kroky k migraci integrací do migrovaného prostředí.
- Vytvořte si podrobný kontrolní seznam, který nastíní proces vyjmutí pro vaši migraci.
- Naplánujte si přiměřené množství prostojů vaší firmy při migraci.
- Důrazně doporučujeme, aby zákazníci s certifikací FastTrack spolupracovali se svým architektem řešení FastTrack a získali pomoc s dohledem nad procesem migrace.
- Důrazně doporučujeme, abyste před provedením první migrace obnovili sandboxové prostředí v samostatné infrastruktuře. Tato aktualizace by měla zahrnovat vaše prostředí Dataverse, které je připojeno k sandboxovému prostředí, do něhož plánujete migrovat.
- Důrazně doporučujeme, abyste při nasazování, migraci a vytváření projektu Lifecycle Services používali účet služby.
- Plánujte upgrade sandboxového prostředí pro ověřování UAT na nejnovější verzi obecné dostupnosti (GA). Další informace viz [Na co brát ohled](hr-infrastructure-merge.md#considerations).
