---
title: "Synchronizace projektových smluv a projektů přímo z Project Service Automation do aplikace Finance and Operations"
description: "Toto téma popisuje šablonu a základní úlohy, které se používají k synchronizaci projektových smluv a projektů přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: 0889bc233674cb80dd056ac77edb5c936c6633a7
ms.contentlocale: cs-cz
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizace projektových smluv a projektů přímo z Project Service Automation do aplikace Finance and Operations

[!include[banner](../includes/banner.md)]

Toto téma popisuje šablonu a základní úlohy, které se používají k synchronizaci projektových smluv a projektů přímo z aplikace Microsoft Dynamics 365 for Project Service Automation do aplikace Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE] 
> Pokud používáte aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, musíte si nainstalovat KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Tok dat pro Project Service Automation a aplikaci Finance and Operations

> [!NOTE]
> Před použitím řešení integrace Project Service Automation do Finance and Operations byste se měli seznámit s funkcí integrace dat Microsoft Dynamics 365.

Řešení integrace Project Service Automation do Finance and Operations používá funkci integrace dat k synchronizaci dat mezi instancemi Project Service Automation and Finance and Operations. Šablona integrace, která jsou k dispozici s funkcí integrace dat, povoluje tok dat o projektech, projektových smlouvách, řádcích smlouvy projektu, a milnících řádků smlouvy projektu z aplikace Project Service Automation do Finance and Operations.

Následující obrázek znázorňuje, jak jsou synchronizována data mezi Project Service Automation a Finance and Operations.

[![Tok dat pro integraci Project Service Automation s aplikací Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Šablony a úkoly

Chcete-li získat přístup k dostupným šablonám, zvolte v centru správy Microsoft PowerApps **Projekty**a v pravém horním rohu vyberte **Nový projekt** pro volbu veřejných šablon.

K synchronizaci projektových smluv a projektů z aplikace Project Service Automation do aplikace Finance and Operations slouží následující šablona a základní úkoly:

- **Název šablony v integraci dat:** Projekty a smlouvy (PSA do Fin and Ops)
- **Název úkolů v projektu:**

    - Projektové smlouvy PSA do Fin and Ops
    - Projekty PSA do Fin and Ops
    - Řádky projektové smlouvy PSA do Fin and Ops
    - Milníky řádků projektové smlouvy PSA do Fin and Ops

Než dojde k synchronizaci projektů a projektových smluv, je nutné synchronizovat účty.

## <a name="entity-set"></a>Sada entit

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| Objednávky                           | Entita integrace pro smlouvu projektu                |
| Projekty                         | Entita integrace pro projekt                         |
| Řádky objednávky                      | Entita integrace pro řádek smlouvy projektu           |
| Milníky řádku smlouvy projektu | Entita integrace pro milník řádků smlouvy projektu |

## <a name="entity-flow"></a>Tok entity

Projektové smlouvy jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako projektové smlouvy. Jako součást šablony integrace lze nastavit zdroj integrace v aplikaci Finance and Operations pro projektovou smlouvu.

Projekty určené časem a materiálem a projekty s pevnou cenou jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako projekty. Jako součást šablony integrace lze nastavit zdroj integrace v aplikaci Finance and Operations pro projekt.

Řádky projektové smlouvy jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako pravidla účtování smlouvy. Synchronizace aktualizuje typ projektu pro projekt řádku smlouvy a skupinu projektů, pokud je metoda účtování odlišná od výchozího typu projektu.

Milníky řádků projektové smlouvy jsou spravovány v Project Service Automation a jsou synchronizovány do Finance and Operations jako milníky pravidel účtování smlouvy.

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Řešení integrace Project Service Automation do aplikace Finance and Operations

Pole **ID smlouvy projektu** je k dispozici na stránce **Projektové smlouvy**. Toto pole slouží jako fyzický a jedinečný klíč k podpoře integrace.

Když je vytvořena nová projektová smlouva a pokud hodnota **ID smlouvy projektu** ještě neexistuje, je automaticky generováno pomocí číselné řady. Hodnota se skládá z údaje **ORD** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Zde je příklad: **ORD-01022-Z4M9Q0**.

Pole **Číslo projektu** je k dispozici na stránce **Projekty**. Toto pole slouží jako fyzický a jedinečný klíč k podpoře integrace.

Když je vytvořen nový projekt a pokud hodnota **Číslo projektu** ještě neexistuje, je automaticky generováno pomocí číselné řady. Hodnota se skládá z údaje **PRJ** a následně dalšího čísla číselné řady, a pak přípony šest znaků. Zde je příklad: **PRJ-01049-CCNID0**.

Když se použije řešení integrace Project Service Automation to Finance and Operations<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, skript upgradu nastaví pole **ID smlouvy projektu** pro existující projektové smlouvy a pole **Číslo projektu** pro existující projekty v Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Nastavení mapování a předpokladů

- Než dojde k synchronizaci projektů a projektových smluv, je nutné synchronizovat účty.
- V nastavení připojení přidejte mapování pole integračního klíče pro **msdyn\_organizationalunits** do **msdyn\_name \[Name\]**. Nejprve bude pravděpodobně nutné přidat projekt k nastavení připojení. Další informace naleznete v tématu [Integrace dat do Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- V nastavení připojení přidejte mapování pole integračního klíče pro **msdyn\_projects** do **msdynce\_projectnumber \[Project Number\]**. Nejprve bude pravděpodobně nutné přidat projekt k nastavení připojení. Další informace naleznete v tématu [Integrace dat do Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).
- **SourceDataID** pro projektové smlouvy a projekty může být aktualizováno na jinou hodnotu nebo odstraněno z mapování. Výchozí hodnota šablony je **Project Service Automation**.
- Mapování **PaymentTerms** musí být aktualizováno tak, aby odráželo platné platební podmínky v aplikaci Finance and Operations. Dále je možné odebrat mapování z úkolu projektu. Výchozí mapa hodnot má výchozí hodnoty pro ukázková data. Následující tabulka zobrazuje hodnoty v Project Service Automation.

    | Hodnota | popis   |
    |-------|---------------|
    | 1     | Čistá 30        |
    | 2     | 2%10, netto 30 |
    | 3     | Čistá 45        |
    | 4     | Čistá 60        |

## <a name="power-query"></a>Power Query

K filtrování dat musíte použít Microsoft Power Query pro Excel, pokud jsou splněny následující podmínky:

- Máte prodejní objednávku v Microsoft Dynamics 365 for Sales.
- Máte několik organizačních jednotek v Project Service Automation a tyto organizační jednotky budou namapovány na více právnických osob v Finance and Operations.

Pokud musíte použít Power Query, postupujte podle následujících pokynů:

- Šablona projektů a smluv (PSA do Fin and Ops) má výchozí filtr, který bude zahrnovat pouze prodejní objednávky typu **Work item (msdyn\_ordertype = 192350001)**. Tento filtr pomáhá zajistit, že projektové smlouvy nejsou vytvořeny pro prodejní objednávky v aplikaci Finance and Operations. Pokud vytvoříte vlastní šablony, je nutné přidat tento filtr.
- Je nutné vytvořit filtr Power Query, který obsahuje pouze organizace smlouvy, které mají být synchronizovány do právnické osoby nastavení připojení integrace. Například projektové smlouvy, které máte s organizační jednotkou smlouvy Contoso USA, by měly být synchronizovány s právnickou osobou USSI, ale projektové smlouvy, které máte s organizační jednotkou kontraktu Contoso Global, by měly být synchronizovány s právnickou osobou USMF. Pokud tento filtr nepřidáte do mapování úkolů, budou všechny smlouvy projektu synchronizovány do právnické osoby definované pro sadu připojení, bez ohledu na organizační jednotku smlouvy.

## <a name="template-mapping-in-data-integration"></a>Mapování šablony v integraci dat

> [!NOTE] 
> Pole **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** a **AddressZipCode** nejsou zahrnuta ve výchozím mapování pro projektové smlouvy. Mapování můžete přidat, pokud potřebujete, aby byly tyto údaje synchronizovány pro smlouvy projektu.
>
> Pole **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fnejsou zahrnuta ve výchozím mapování pro projekty. Mapování můžete přidat, pokud potřebujete, aby byly tyto údaje synchronizovány pro projekty.

Na následujícím obrázku je příklad mapování úkolu šablony v integraci dat. Mapování ukazuje, jaké informace o poli budou synchronizovány z aplikace Project Service Automation do aplikace Finance and Operations.

[![Mapování šablony](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapování šablony](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapování šablony](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapování šablony](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

