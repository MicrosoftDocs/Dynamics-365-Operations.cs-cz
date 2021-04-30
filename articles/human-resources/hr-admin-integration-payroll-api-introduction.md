---
title: Úvod do rozhraní API integrace mezd
description: Toto téma popisuje rozhraní API Dynamics 365 Human Resources pro integraci mezd.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61b90c566325bb8d83b09fceebc721cfb14d3fc8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891119"
---
# <a name="payroll-integration-api-introduction"></a>Úvod do rozhraní API integrace mezd

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento dokument popisuje rozhraní API Dynamics 365 Human Resources pro integraci mezd. API umožňuje efektivní přímou integraci mezi systémy Human Resources a mzdovými systémy partnerů. Integrované prostředí začíná v Human Resources profilem zaměstnanců, platem a srážkami a informacemi o příspěvcích. Když si najmete zaměstnance a zadáte požadovaný profil a informace o platu do Human Resources, mzdový systém tyto informace použije při zpracování mezd. Veškeré aktualizace provedené v informacích o zaměstnancích nebo výplatách jsou také staženy pro použití v pozdějších výplatách.

![Tok integrace mezd](media/hr-admin-integration-payroll-api-introduction-flow.png)

Aby bylo možné integraci povolit, v modulu Human Resources jsou přidány tyto komponenty:

- Funkce pro označení zaměstnance jako připraveného k výplatě
- Rozhraní API pro integraci, které otevírá nové funkce pro integraci aplikací

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Toto rozhraní API je postaveno na Microsoft Dataverse (dříve Common Data Service). Veškerá interakce RESTful s tímto API probíhá prostřednictvím webového rozhraní Microsoft Dataverse Web API, které používá OData. Toto rozhraní API je podmnožinou webového rozhraní Dataverse Web API. Dataverse Web API definuje charakteristiky, jako je ověřování, smlouvy SLA, dávka, řízení souběžnosti a zpracování chyb.

Další obecné informace o webovém rozhraní Microsoft Dataverse Web API viz:

- [Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Použití webového rozhraní Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)
- [Průvodce vývojáře Microsoft Dataverse](/powerapps/developer/data-platform)

Tato dokumentace obsahuje podrobnosti a pokyny pro vývojáře k používání webového rozhraní Dataverse, včetně následujících témat:

- [Ověření pro Microsoft Dataverse s webovým API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Provádění operací pomocí webového rozhraní API](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Použití Postmana s webovým rozhraní API](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Pomocí sledování změn můžete synchronizovat data s externími systémy](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuální tabulky pro Human Resources v Dataverse

Koncové body rozhraní API pro integraci mezd využívají možnosti platformy virtuálních tabulek Microsoft Dataverse. Ve výchozím nastavení nejsou virtuální tabulky a jejich přidružené koncové body rozhraní API nasazeny pro prostředí Human Resources, což organizacím umožňuje určit, které koncové body OData budou pro dané prostředí k dispozici. Chcete-li použít rozhraní API, musí být pro prostředí vygenerovány virtuální tabulky pro entity Human Resources.

Informace o generování virtuálních tabulek pro rozhraní API najdete v části [Konfigurace virtuálních tabulek Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Datový model

Následující diagramy ukazují vztahy v rámci rozhraní API. Několik typů má cizí klíče k jiným, již existujícím entitám v modulu Human Resources, které zde nejsou znázorněny. Tento dokument poskytuje informace o entitách, které jsou specifické pro scénáře integrace mezd. Existuje však mnoho dalších entit ve webovém rozhraní API Dataverse pro Human Resources, které mohou být pro integraci rovněž relevantní. Na některé z těchto entit se odkazuje ve vztazích cizích klíčů nebo ve vlastnostech navigace.

![Datový model rozhraní API pro integraci mezd](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a>Zaměstnanec na výplatní listině a související entity

Entity:

- [Zaměstnanec na výplatní listině](hr-admin-integration-payroll-api-payroll-employee.md)
- [Adresa pracovníka na výplatní listině](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Mzdový plán fixní kompenzace](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Práce pozice mzdy](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Pozice mzdy](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Viz také

[Generování a kontrola entit mzdy](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Konfigurace parametrů Human Resources](hr-setup-parameters.md)<br>
[Konfigurace sdílených parametrů Human Resources](hr-setup-shared-parameters.md)<br>
[Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Použití webového rozhraní Microsoft Dataverse Web API](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]