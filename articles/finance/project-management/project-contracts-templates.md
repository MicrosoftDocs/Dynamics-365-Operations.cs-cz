---
title: Synchronizace projektových smluv a projektů přímo z Project Service Automation do aplikace Finance and Operations
description: Toto téma popisuje šablonu a základní úkoly, které se používají k synchronizaci smluv o projektech a projektů přímo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 76c62f3a503ff2a8c93143390fc91ef81fbf7d0f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250454"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizace projektových smluv a projektů přímo z Project Service Automation do aplikace Finance and Operations

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablonu a základní úkoly, které se používají k synchronizaci smluv o projektech a projektů přímo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.

> [!NOTE] 
> Pokud používáte Enterprise edition 7.3.0, je nutné nainstalovat KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok dat pro Project Service Automation a aplikaci Finance

> [!NOTE]
> Před použitím řešení integrace Project Service Automation to Finance and Operations byste se měli seznámit s funkcí integrace dat Dynamics 365.

Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation a Finance. Šablona integrace, která jsou k dispozici s funkcí integrace dat, povoluje tok dat o projektech, projektových smlouvách, řádcích smlouvy projektu, a milnících řádků smlouvy projektu z aplikace Project Service Automation do Finance.

Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance.

[![Tok dat pro integraci Project Service Automation s aplikací Finance](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft PowerApps **Projekty** a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.

K synchronizaci projektových smluv a projektů z aplikace Project Service Automation do aplikace Finance slouží následující šablony a základní úkoly:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrace s Dynamics 365 Project Service Automation v2. x
- **Název šablony v integraci dat:** Projekty a smlouvy (PSA do Fin and Ops)
- **Název úkolů v projektu:**

    - Projektové smlouvy PSA do Fin and Ops
    - Projekty PSA do Fin and Ops
    - Řádky projektové smlouvy PSA do Fin and Ops
    - Milníky řádků projektové smlouvy PSA do Fin and Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrace s Dynamics 365 Project Service Automation v3.x
V Project Service Automation došlo ke změně schématu, která má vliv na šablonu milníku řádku smlouvy aplikace Projekt a je potřeba použití verze v2 šablony pro integraci Project Service Automation v3.x s Dynamics 365.

- **Název šablony v integraci dat:** Projekty a smlouvy (PSA 3.x do Fin and Ops)- v2
- **Název úkolů v projektu:**

    - Projektové smlouvy PSA do Fin and Ops
    - Projekty PSA do Fin and Ops
    - Řádky projektové smlouvy PSA do Fin and Ops
    - Milníky řádků projektové smlouvy PSA do Fin and Ops

Než dojde k synchronizaci projektů a projektových smluv, je nutné synchronizovat účty.

## <a name="entity-set"></a>Sada entit

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Objednávky                           | Entita integrace pro smlouvu projektu                |
| Projekty                         | Entita integrace pro projekt                         |
| Řádky objednávky                      | Entita integrace pro řádek smlouvy projektu           |
| Milníky řádku smlouvy projektu | Entita integrace pro milník řádků smlouvy projektu |

## <a name="entity-flow"></a>Tok entity

Projektové smlouvy jsou spravovány v Project Service Automation a jsou synchronizovány do Finance jako projektové smlouvy. Jako součást šablony integrace lze nastavit zdroj integrace v aplikaci Finance pro projektovou smlouvu.

Projekty určené časem a materiálem a projekty s pevnou cenou jsou spravovány v Project Service Automation a jsou synchronizovány do Finance jako projekty. Jako součást šablony integrace lze nastavit zdroj integrace v aplikaci Finance pro projektovou smlouvu.

Řádky projektové smlouvy jsou spravovány v Project Service Automation a jsou synchronizovány do Finance jako pravidla účtování smlouvy. Synchronizace aktualizuje typ projektu pro projekt řádku smlouvy a skupinu projektů, pokud je metoda účtování odlišná od výchozího typu projektu.

Milníky řádků projektové smlouvy jsou spravovány v Project Service Automation a jsou synchronizovány do Finance jako milníky pravidel účtování smlouvy.

## <a name="project-service-automation-to-finance-integration-solution"></a>Řešení integrace Project Service Automation do aplikace Finance

Pole **ID smlouvy projektu** je k dispozici na stránce **Projektové smlouvy**. Toto pole slouží jako fyzický a jedinečný klíč k podpoře integrace.

Když je vytvořena nová projektová smlouva a pokud hodnota **ID smlouvy projektu** ještě neexistuje, je automaticky generováno pomocí číselné řady. Hodnota se skládá z údaje **ORD** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Zde je příklad: **ORD-01022-Z4M9Q0**.

Pole **Číslo projektu** je k dispozici na stránce **Projekty**. Toto pole slouží jako fyzický a jedinečný klíč k podpoře integrace.

Když je vytvořen nový projekt a pokud hodnota **Číslo projektu** ještě neexistuje, je automaticky generováno pomocí číselné řady. Hodnota se skládá z údaje **PRJ** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Zde je příklad: **PRJ-01049-CCNID0**.

Když se použije řešení integrace Project Service Automation do Finance, skript upgradu nastaví pole **ID smlouvy projektu** pro existující projektové smlouvy a pole **Číslo projektu** pro existující projekty v Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

- Než dojde k synchronizaci projektů a projektových smluv, je nutné synchronizovat účty.
- V nastavení připojení přidejte mapování pole integračního klíče pro **msdyn\_organizationalunits** do **msdyn\_name \[Name\]**. Nejprve bude pravděpodobně nutné přidat projekt k nastavení připojení. Další informace naleznete v tématu [Integrace dat do Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- V nastavení připojení přidejte mapování pole integračního klíče pro **msdyn\_projects** do **msdynce\_projectnumber \[Project Number\]**. Nejprve bude pravděpodobně nutné přidat projekt k nastavení připojení. Další informace naleznete v tématu [Integrace dat do Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- **SourceDataID** pro projektové smlouvy a projekty může být aktualizováno na jinou hodnotu nebo odstraněno z mapování. Výchozí hodnota šablony je **Project Service Automation**.
- Mapování **PaymentTerms** musí být aktualizováno tak, aby odráželo platné platební podmínky v aplikaci Finance. Dále je možné odebrat mapování z úkolu projektu. Výchozí mapa hodnot má výchozí hodnoty pro ukázková data. Následující tabulka zobrazuje hodnoty v Project Service Automation.

    | Hodnota | popis   |
    |-------|---------------|
    | 1     | Čistá 30        |
    | 2     | 2% 10, netto 30 |
    | 3     | Čistá 45        |
    | 4     | Čistá 60        |

## <a name="power-query"></a>Power Query

K filtrování dat musíte použít Microsoft Power Query pro Excel, pokud jsou splněny následující podmínky:

- Máte prodejní objednávku v Dynamics 365 Sales.
- Máte několik organizačních jednotek v Project Service Automation a tyto organizační jednotky budou namapovány na více právnických osob v Finance.

Pokud musíte použít Power Query, postupujte podle následujících pokynů:

- Šablona projektů a smluv (PSA do Fin and Ops) má výchozí filtr, který bude zahrnovat pouze prodejní objednávky typu **Work item (msdyn\_ordertype = 192350001)**. Tento filtr pomáhá zajistit, že projektové smlouvy nejsou vytvořeny pro prodejní objednávky v aplikaci Finance. Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr.
- Je nutné vytvořit filtr Power Query, který obsahuje pouze organizace smlouvy, které mají být synchronizovány do právnické osoby nastavení připojení integrace. Například projektové smlouvy, které máte s organizační jednotkou smlouvy Contoso USA, by měly být synchronizovány s právnickou osobou USSI, ale projektové smlouvy, které máte s organizační jednotkou kontraktu Contoso Global, by měly být synchronizovány s právnickou osobou USMF. Pokud tento filtr nepřidáte do mapování úkolů, budou všechny smlouvy projektu synchronizovány do právnické osoby definované pro sadu připojení, bez ohledu na organizační jednotku smlouvy.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

> [!NOTE] 
> Pole **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** a **AddressZipCode** nejsou zahrnuta ve výchozím mapování pro projektové smlouvy. Mapování můžete přidat, pokud potřebujete, aby byly tyto údaje synchronizovány pro smlouvy projektu.
>
> Pole **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fnejsou zahrnuta ve výchozím mapování pro projekty. Mapování můžete přidat, pokud potřebujete, aby byly tyto údaje synchronizovány pro projekty.

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance.

[![Mapování šablony](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapování šablony](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapování šablony](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapování šablony](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mapování milníku řádku smlouvy projektu v aplikaci Projects and Contracts (PSA 3.x do Dynamics) - šablona v2:

[![Mapování šablony](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
