---
title: Volba technologie integrace dat
description: Tento článek poskytuje návod k různým možnostem integrace s daty spravovanými aplikací Human Resources, který popisuje charakteristické rysy různých integračních technologií, aby mohli integrátoři činit informovaná rozhodnutí o tom, které technologie nejlépe vyhovují jejich potřebám.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f2de5dd41c00e6546b4a4feadaf5774430d572bb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029881"
---
# <a name="choose-a-data-integration-technology"></a>Volba technologie integrace dat

Dynamics 365 Human Resources spravuje obchodní data, která jsou užitečná v různých obchodních procesech. Tento článek poskytuje návod k různým možnostem integrace s daty spravovanými aplikací Human Resources, který popisuje charakteristické rysy různých integračních technologií, aby mohli integrátoři činit informovaná rozhodnutí o tom, které technologie nejlépe vyhovují jejich potřebám.

## <a name="data-integration-vision"></a>Vize integrace dat

Společnost Microsoft vnímá obchodní data jako klíčový prostředek, který činí vaši společnost jedinečnou. Data vašeho podniku jsou velice cenná. Data shromažďovaná a udržovaná jednou částí podniku se vztahují k datům shromažďovaným jinou částí podniku a tyto vztahy lze využít ke zlepšení obchodních procesů a analytických nástrojů v rámci organizace. Zajištění snadného, bezpečného a stabilního přístupu k vašim obchodním datům, bez ohledu na to, který systém tato data „vlastní”, je hlavní princip uplatňovaný v rámci naší vize integrace dat s aplikací Human Resources.

V minulosti byla integrace dat mezi více systémy obtížná.
Společnost Microsoft činí kroky, které usnadňují integraci dat, a velkým krokem k uskutečnění tohoto cíle je použití služby [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Aplikace Human Resources postupně činí ze služby Common Data Service upřednostňované veřejné rozhraní pro data aplikace Human Resources. Očekáváme, že všechna nejdůležitější data spravovaná aplikací Human Resources budou v průběhu času zpřístupněna ve službě Common Data Service. Doporučujeme službu Common Data Service jako preferovanou technologii pro většinu typů uplatnění v rámci integrace dat. I když si uvědomujeme, že ne všechna data vyžadovaná pro váš typ použití jsou ve službě Common Data Service momentálně přítomna a že časové harmonogramy vašich projektů mohou vyžadovat použití alternativní technologie, informujte nás, pokud služba Common Data Service nesplňuje vaše potřeby související s integrací.

## <a name="integration-technologies"></a>Integrační technologie

V následujících částech jsou popsány různé technologie integrace dat, které jsou k dispozici pro použití s aplikací Human Resources.

### <a name="common-data-service-entities"></a>Entity služby Common Data Service

Služba Common Data Service je preferované veřejné datové rozhraní pro aplikaci Human Resources. Služba Common Data Service je postavena na vyspělé platformě a byla vytvořena z platformy Dynamics 365 „XRM”, na které jsou postavena řešení [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement).

Služba Common Data Service poskytuje platformu pro datové entity a rozhraní API pro přístup k těmto entitám. Je-li aplikace Human Resources nasazena v rámci vaší organizace, je připojena k instanci služby Common Data Service a entity spravující data aplikace Human Resources jsou nasazeny v této instanci služby Common Data Service, díky čemuž jsou entity a jejich data zpřístupněny libovolné aplikaci, která se může připojit k instanci služby Common Data Service. V závislosti na tom, které aplikace Human Resources používáte, provádějí tyto aplikace operace s daty buďto přímo na entitách služby Common Data Service (to platí pro aplikace Attract a Onboard) nebo synchronizují data s entitami Common Data Service, a to oběma směry.

Jsou-li datové entity zpřístupňující data vyžadovaná vašimi integračními aplikacemi přítomné ve službě Common Data Service, můžete plně využívat služby [Common Data Service a rozhraní API, která služba podporuje](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Mezi podporovaná rozhraní API patří [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), které poskytuje implementaci OData pro přístup k datům služby Common Data Service.

Entity služby Common Data Service a přidružená rozhraní API jsou nejlepší možností pro přístup k datům aplikací Human Resources prostřednictvím webových aplikací, webových služeb / rozhraní API a libovolné další aplikace, která se připojuje ke kanálům OData.

> [!NOTE]
> Vzhledem k tomu, že rozhodnutí učinit ze služby Common Data Service preferované datové rozhraní pro aplikace Human Resources bylo učiněno poměrně nedávno, můžete zjistit, že datové entity aplikací Human Resources, které potřebujete pro vaši integraci, dosud nejsou ve službě Common Data Service<sup>1</sup> přítomné. Pokud entity aplikací Human Resources nezbytné pro integraci nejsou dosud k dispozici, budete muset počkat na zpřístupnění těchto datových entit nebo budete muset použít některou z dalších integračních technologií, které jsou popsány níže.
> 
> Ve výchozím nastavení je integrace pomocí služby Common Data Service v nových prostředích, která neobsahují poskytnutá ukázková data, zakázána. U nových prostředí obsahujících ukázková data je tato integrace zapnutá a tato prostředí začínají synchronizovat data, jakmile jsou poskytnuta. Jakmile je vaše prostředí připraveno k synchronizaci dat, můžete spustit integraci.

<sup>1</sup>Seznam entit aplikací Human Resources, které jsou k dispozici ve službě Common Data Service, viz  [Human Resources a Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities). V případě aplikací Attract a Onboard jsou ve službě Common Data Service k dispozici všechny entity.

### <a name="dmfdixf-entities"></a>Entity DMF/DIXF

Aplikace Human Resources, postavená primárně na stejné platformě jako aplikace Finance and Operations, poskytuje [Data Management Framework(DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json), jež se někdy uvádí pod názvem Data Import Export Framework nebo DIXF, a soubor datových entit, které mohou být použity pro import/export dat do/z aplikace Human Resources. Zatímco entity služby Common Data Service jsou preferovaným rozhraním integrace dat pro aplikaci Human Resources, entity DMF budou i nadále za určitých okolností užitečné. Jedná se například o tyto případy:

- Entity služby Common Data Service dosud nejsou k dispozici.

- Integrace vyžaduje funkce pro hromadný import a export dat s vysokým výkonem.

Entity DMF aktuálně poskytují nejúplnější pokrytí pro data aplikace Human Resources.

DMF se nehodí pro integraci v reálném čase (například je-li vyžadována okamžitá zpětná vazba uživatele v uživatelském rozhraní), protože operace s balíčkem jsou plánované dávkové úlohy a budou mít často prodlevu minimálně 1–2 minuty předtím, než dávková služba převezme úlohu k provedení, k čemuž se přičítá čas nezbytný pro provedení operace importu/exportu.

DMF může být nejlepší volbou v případě vysoké požadované propustnosti (například při nočním naplánovaném importu/exportu mnoha tisíc záznamů).

> [!NOTE]
> DMF není k dispozici pro aplikaci Attract a Onboard.

### <a name="dmf-package-rest-api"></a>Rozhraní REST API balíčku DMF

DMF poskytuje rozhraní [REST API](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) pro manipulaci s datovými balíčky. Toto rozhraní API lze použít k interakci programu s DMF, jež umožňuje například níže uvedené akce:

- Import datového balíčku.

- Export datového balíčku.

- Kontrola stavu operace importu/exportu.

Rozhraní REST API balíčku DMF je plně podporováno v aplikacích Human Resources: Core HR.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF dále poskytuje výkonnou funkci (obecně známou jako [dodejte svou vlastní databázi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) nebo BYOD), která umožňuje aplikacím Human Resources exportovat data do vaší vlastní SQL databáze Microsoft Azure. Tato funkce poskytuje značnou flexibilitu, protože v případě přítomnosti dat ve vaší vlastní SQL databázi můžete využívat libovolné aplikace nebo middleware, které se mohou připojit k úložišti dat SQL.

BYOD by se obecně mělo považovat za řešení určené jen pro čtení. I když jste schopni manipulovat s libovolnými daty v SQL databázi Azure a ukládat je (například kombinacemi více datových zdrojů), data uložená v SQL databázi Azure nebudou synchronizována zpět s aplikacemi Human Resources.

BYOD je vhodné pro řešení vykazování, integraci dat a kombinace více datových zdrojů jako datového zdroje pro pipeline [Azure Data Factory.](https://docs.microsoft.com/azure/data-factory/).

> [!NOTE]
> BYOD není k dispozici pro aplikaci Attract a Onboard.

### <a name="odata-enabled-entities"></a>Entity s povolenou službou OData

Většina entit DMF je také povolena pro přístup prostřednictvím datové služby (OData) aplikací Human Resources. Dokumentace dostupná pro [Finance and Operations službu OData](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata) se obecně také týká aplikací Human Resources, ačkoli dokumentace týkající se vytváření vašich vlastních entit zpřístupněných pro službu OData se těchto aplikací netýká.

I když je služba Common Data Service a implementace služby OData poskytovaná službou Common Data Service (prostřednictvím [Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) preferována před datovou službou aplikace Human Resources, datová služba aplikace Human Resources má momentálně úplnější pokrytí entit pro data aplikace Human Resources.

### <a name="excel-add-in"></a>Doplněk pro aplikaci Excel

[Doplněk pro aplikaci Excel](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) využívá entity s povolenou službou OData pod povrchem. Umožňuje koncovému uživateli snadno načíst a upravit data aplikace Human Resources pomocí známého uživatelského rozhraní aplikace Excel.

Doplněk pro aplikaci Excel je vhodný pro ad-hoc importy/exporty dat prováděné odborníky na byznys doménu. Pro opakující se integraci dat, která vyžaduje automatizaci s využitím programu, bude vhodnější další integrační technologie.

### <a name="data-integrator"></a>Služba Data Integrator

Prostředí správce služby Common Data Service poskytuje [službu Data Integrator](https://docs.microsoft.com/powerapps/administrator/data-integrator), kterou lze použít k integraci dat se službou Common Data Service, a to oběma směry. Službu Data Integrator lze použít k definování integračních projektů (často na základě předdefinovaných šablon, které vývojáři aplikací přizpůsobili pro konkrétní integrace). Projekty integrace lze naplánovat tak, aby se spouštěly automaticky na základě opakujícího se harmonogramu, nebo mohou být spouštěny ručně.

Projekty služby Data Integrator jsou vhodné pro dávkové integrace pomocí služby Common Data Service a jsou skvělou volbou pro integrace mezi řadou aplikací Dynamics 365. Například společnost Microsoft poskytuje přednastavenou šablonu služby Data Integrator, kterou lze použít k integraci dat z aplikace Human Resources do aplikace Dynamics 365 Finance. Další informace viz [Integrace ze služby Dynamics 365 Human Resources do služby Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Služba Data Integrator také podporuje [nástroj Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) (prostřednictvím své [funkce Advanced Query](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering)).
Nástroj Power Query poskytuje výkonné a flexibilní filtrování a transformace dat, včetně bohatého jazyka M formula language, a pravděpodobně bude znám uživatelům, kteří mají zkušenosti s vývojem záznamů Power BI.

## <a name="deciding-on-an-integration-technology"></a>Rozhodování o technologii integrace

V případě, že je k dispozici mnoho různých integračních technologií, může být rozhodování o volbě přístupu k integraci někdy velmi intenzivní. V průběhu času, a zejména s rozvojem datového pokrytí ve službě Common Data Service, se bude rozhodování neustále ulehčovat, přičemž služba Common Data Service bude ve většině případů preferované datové rozhraní. Avšak do té doby můžete zjistit, že služba Common Data Service dosud nesplňuje vaše potřeby. Následující tabulka pomáhá při shrnutí některých hlavních charakteristik různých možností integračních technologií.

| Technologie / nástroj / rozhraní API    | Opakované integrace                   | Synchronní/asynchronní                    | Programový přístup prostřednictvím rozhraní API        | Vhodné datové objemy                                   | Datové pokrytí                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Entity služby Common Data Service           | Ano, pomocí služby Data Integrator nebo middlewaru | Synch. asynch., dávkově (prostřednictvím služby Data Integrator) | Ano, prostřednictvím Dynamics 365 Web API (OData) | Liší se podle jednotlivých případů použití (podporuje stránkování v případě interaktivního použití) | Vylepšení<sup>2</sup>                       |
| Entity DMF           | Ano, plánováno prostřednictvím middlewaru        | Asynch., dávka                                | Ano, prostřednictvím rozhraní REST API balíčku DMF         | Vysoké (stovky tisíc záznamů)                    | Vysoké                                |
| Rozhraní REST API balíčku DMF   | Ano, plánováno prostřednictvím middlewaru        | Asynch., dávka                                | Ano                                       | Vysoké (stovky tisíc záznamů)                    | Rozhraní API podporuje všechny entity DMF.       |
| BYOD                   | Ano, plánováno správcem v aplikaci Human Resources        | Asynch., dávka                                | Ne<sup>3</sup>                                    | Vysoké (stovky tisíc záznamů)                    | Podporuje všechny entity DMF.           |
| Entity s povolenou službou OData | Ano, použití middlewaru                    | Synchronizovat                                        | Ano, prostřednictvím datové služby (OData) aplikace Human Resources  | Liší se podle jednotlivých případů použití (podporuje stránkování v případě interaktivního použití) | Vysoké                                |
| Doplněk pro aplikaci Excel           | Ne                                       | Synchronizovat                                        | Ne                                        | Střední (desítky tisíc záznamů)                      | Podporuje všechny entity s povolenou službou OData. |
| Služba Data Integrator        | Ano, plánováno ve službě Data Integrator        | Asynch., dávka                                | Ne                                        | Liší se podle případu použití.                                       | Podporuje všechny entity služby Common Data Service.           |

<sup>2</sup>Společnost Microsoft intenzivně investuje do zvýšení datového pokrytí pro entity služby Common Data Service a doporučuje službu Common Data Service jako preferované datové rozhraní v případě, že je k dispozici pokrytí. Služba Common Data Service poskytuje v současné době nízké datové pokrytí ve vztahu k DMF a entitám s povolenou službou OData.

<sup>3</sup>SQL databáze je přístupná prostřednictvím programu.

## <a name="summary"></a>Souhrn

Vaše obchodní data představují cenný prostředek, avšak jejich hodnota může být značně snížena, je-li obtížné data využívat ke konkrétním účelům (například vytváření hlášení, kombinování zdrojů dat nebo přizpůsobenému použití). Produkt Dynamics 365 Human Resources poskytuje několik technologií pro práci s vašimi daty mimo uživatelské rozhraní (UI) aplikace Human Resources, které vám umožňují integraci přístupu aplikací k datům. Toto téma popisuje dostupné integrační technologie a některé z jejich hlavních vlastností. Tyto informace vám pomohou lépe rozhodovat o tom, které přístupy ke svým integračním projektům máte využít.

