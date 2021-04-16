---
title: Úvod do rozhraní API pro integraci systému sledování žadatelů
description: Toto téma popisuje rozhraní API pro integraci systému sledování žadatelů (ATS) v Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 599f9728019cd6bc59c59a4f08df06c6c9c9ac31
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798410"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Úvod do rozhraní API pro integraci systému sledování žadatelů

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje rozhraní API pro integraci systému sledování žadatelů (ATS) v Dynamics 365 Human Resources. Účelem rozhraní API je umožnit efektivní integraci mezi Dynamics 365 Human Resources a partnerskými systémy ATS.

![Tok integrace ATS](media/hr-admin-integration-ats-api-introduction-flow.png)

Integrované prostředí začíná v modulu Human Resources, když náborový manažer vytvoří požadavek na nábor. Když je požadavek aktivován, ATS vytáhne podrobnosti o požadavku k vytvoření náborového projektu. Poté dle náborového kanálu vybere a přijme kandidáta na dané pozice. Nakonec ATS dokončí integraci opakovanou cestou zasláním záznamu vybraného kandidáta do modulu Human Resources. Záznam kandidáta pak může projít více ověřeními a pracovními postupy náboru, než je vytvořen záznam zaměstnance.

Aby bylo možné integraci povolit, v modulu Human Resources jsou přidány tyto komponenty:

1.  Funkce pro vytvoření žádosti o nábor.
2.  Rozšířený profil kandidáta a související pracovní postupy.
3.  Rozhraní API pro integraci, které otevírá nové funkce pro integraci aplikací.

Další informace o nastavení a používání funkce žádosti o nábor a práci s kandidáty najdete v tématu [Nábor uchazečů o práci](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Toto rozhraní API je postaveno na Microsoft Dataverse (dříve Common Data Service). Veškerá interakce RESTful s tímto API probíhá prostřednictvím webového rozhraní Microsoft Dataverse Web API, které používá OData. Toto rozhraní API je podmnožinou webového rozhraní Dataverse Web API. Dataverse Web API definuje charakteristiky, jako je ověřování, smlouvy SLA, dávka, řízení souběžnosti a zpracování chyb.

Další obecné informace o webovém rozhraní Microsoft Dataverse Web API viz:

- [Co je Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [Použití webového rozhraní Microsoft Dataverse Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [Průvodce vývojáře Microsoft Dataverse](https://docs.microsoft.com/powerapps/developer/data-platform)

Výše uvedená dokumentace obsahuje podrobnosti a pokyny pro vývojáře ohledně použití webového rozhraní Dataverse Web API, jako je [správa ověřování](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [provádění operací](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [použití platformy Postman s tímto rozhraním API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) a [použití sledování změn nebo delta tokenů](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) s daným rozhraním API.

### <a name="option-sets"></a>Sada možností

Datový model rozhraní API pro integraci ATS popsaný v tomto dokumentu obsahuje sady možností, které poskytují výčtové hodnoty přidružené k vlastnostem entity. Podrobnosti o práci se sadami možností v Dataverse Web API viz [Vytváření a aktualizace sad možností pomocí webového rozhraní API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets). Sady možností jsou definovány pro každé prostředí Dataverse.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuální tabulky pro Human Resources v Dataverse

Koncové body rozhraní API pro integraci ATS využívají možnosti platformy virtuálních tabulek Microsoft Dataverse. Ve výchozím nastavení nejsou virtuální tabulky a jejich přidružené koncové body rozhraní API nasazeny pro prostředí Human Resources, což organizacím umožňuje určit, které koncové body OData budou pro dané prostředí k dispozici. Chcete-li použít rozhraní API, musí být pro prostředí vygenerovány virtuální tabulky pro entity Human Resources. 

Informace o generování virtuálních tabulek pro rozhraní API najdete v části [Konfigurace virtuálních tabulek Dataverse](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="data-model"></a>Datový model

Datový model je soustředěn kolem dvou hlavních entit:

- **RecruitingRequest** představuje žádost na ATS o nábor jedné či více otevřených pozic. Ukázkový dotaz viz [Příklad dotazu pro entitu Žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire** představuje podrobnosti o uchazeči, který přijal nabídku na pozici. **Person** představuje osobu, která je kandidátem. Osoba může mít ve společnosti více rolí, jako je kandidát, pracovník, zaměstnanec nebo dodavatel. Příklad dotazu viz [Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

Následující diagramy ukazují vztahy v rámci rozhraní API. Několik typů má cizí klíče k jiným, již existujícím entitám v modulu Human Resources, které zde nejsou znázorněny. Tento dokument poskytuje informace o entitách, které jsou specifické pro scénáře integrace náboru. Existuje však mnoho dalších entit v Dataverse Web API pro Dynamics 365 Human Resources, které mohou být pro integraci rovněž relevantní. Můžete například potřebovat také podrobnosti o pracovnících, pracích, pozicích nebo jiných entitách, které zde nejsou definovány. Na mnoho z těchto entit se odkazuje ve vztazích cizích klíčů nebo ve vlastnostech navigace.

![Datový model rozhraní API pro integraci ATS](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Žádost o nábor a související entity a sady možností

Ukázkový dotaz: 

- [Příklad dotazu na žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Entity:

- [Požadavek na nábor](hr-admin-integration-ats-api-recruiting-request.md)
- [Pozice požadavků na nábor](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Požadavky na zkušenosti pro nábor](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Požadavek na vzdělání při náboru](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Místo požadavku na nábor](hr-admin-integration-ats-api-recruiting-request-location.md)

Sada možností:

- [Stav práce z hlediska přesčasů](hr-admin-integration-ats-api-job-exempt-status.md)
- [Stav pozice v žádosti o nábor](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Stav žádosti o nábor](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Regulační kategorie pracovních míst](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Kandidát k přijetí a související entity a sady možností

Ukázkový dotaz:

- [Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Entity:

- [Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Osoba](hr-admin-integration-ats-api-person.md)
- [Vzdělání osoby](hr-admin-integration-ats-api-person-education.md)
- [Profesionální zkušenosti osoby](hr-admin-integration-ats-api-person-professional-experience.md)
- [Adresa osoby](hr-admin-integration-ats-api-person-address.md)
- [Kontakt strany](hr-admin-integration-ats-api-party-contact.md)
- [Dovednost osoby](hr-admin-integration-ats-api-person-skill.md)
- [Úroveň hodnocení](hr-admin-integration-ats-api-rating-level.md)
- [Certifikát osoby](hr-admin-integration-ats-api-person-certificate.md)
- [Typ certifikátu](hr-admin-integration-ats-api-certificate-type.md)
- [Prověřování osoby](hr-admin-integration-ats-api-person-screening.md)
- [Typy prověřování](hr-admin-integration-ats-api-screening-types.md)
- [Osobní identifikační číslo](hr-admin-integration-ats-api-person-identification-number.md)

Sady možností:

- [Výsledek integrace uchazeče](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Prázdné Ano Ne](hr-admin-integration-ats-api-blank-yes-no.md)
- [Stav dokončení](hr-admin-integration-ats-api-completion-status.md)
- [Typ kontaktu](hr-admin-integration-ats-api-contact-type.md)
- [Základ kreditu vzdělání](hr-admin-integration-ats-api-education-credit-basis.md)
- [Rod](hr-admin-integration-ats-api-gender.md)
- [Rodinný stav](hr-admin-integration-ats-api-marital-status.md)
- [Měsíce roku](hr-admin-integration-ats-api-months-of-year.md)
- [Ne Ano](hr-admin-integration-ats-api-no-yes.md)
- [Jednotka období](hr-admin-integration-ats-api-period-unit.md)
- [Frekvence prověřování](hr-admin-integration-ats-api-screening-frequency.md)
- [Generovat frekvenci prověřování z](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Typ úrovně dovedností](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Viz také

[Nábor uchazečů o práci](hr-personnel-recruit.md)<br>
[Co je Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[Použití webového rozhraní Microsoft Dataverse Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[Vytváření a aktualizace sad možností pomocí webového rozhraní API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]