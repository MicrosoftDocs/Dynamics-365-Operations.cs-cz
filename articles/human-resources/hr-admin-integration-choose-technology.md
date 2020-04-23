---
title: Volba technologie integrace dat
description: Tento článek poskytuje informace o integraci s daty spravovanými v Human Resources. Popisuje různé integrační technologie, které vám pomohou určit, které technologie nejlépe odpovídají vašim potřebám.
author: andreabichsel
manager: AnnBe
ms.date: 02/28/2020
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
ms.openlocfilehash: 6bb754ca80af0a0793b5ee162a378ebbe92524c5
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2020
ms.locfileid: "3197283"
---
# <a name="choose-a-data-integration-technology"></a>Volba technologie integrace dat

Tento článek poskytuje informace o integraci s daty spravovanými v Dynamics 365 Human Resources. Popisuje různé integrační technologie, které vám pomohou určit, které technologie nejlépe odpovídají vašim potřebám.

## <a name="data-integration-background"></a>Pozadí integrace dat

Obchodní data představují klíčový prostředek, který činí vaši společnost jedinečnou. Data vašeho podniku jsou velice cenná. Vztahy mezi daty, která se shromažďují ve vaší společnosti, můžete použít ke zlepšení obchodních procesů a analytických nástrojů v rámci celé společnosti. Usilujeme o zajištění snadného, zabezpečeného a stabilního přístupu k obchodním datům, ať už se jedná o systém, ze kterého pochází.

V minulosti byla integrace dat mezi více systémy obtížná.
Společnost Microsoft činí kroky, které usnadňují integraci dat, a velkým krokem k uskutečnění tohoto cíle je použití služby [Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Human Resources činí ze služby Common Data Service upřednostňované veřejné rozhraní pro data aplikace Human Resources. Očekáváme, že všechna nejdůležitější data spravovaná aplikací Human Resources budou v průběhu času zpřístupněna ve službě Common Data Service. Doporučujeme službu Common Data Service jako preferovanou technologii pro většinu typů uplatnění v rámci integrace dat.

Uvěodmujeme si, že Common Data Service ještě nemusí obsahovat všechna data, která aplikace vyžaduje. Rovněž jsme si uvědomujeme, že časová osa projektu může vyžadovat alternativní technologii. Nezapomeňte nám sdělit, kdy Common Data Service nevyhovuje vašim potřebám integrace.

## <a name="integration-technologies"></a>Integrační technologie

V následujících částech jsou popsány různé technologie integrace dat, které jsou k dispozici pro použití s aplikací Human Resources.

### <a name="common-data-service-entities"></a>Entity služby Common Data Service

Služba Common Data Service je preferované veřejné datové rozhraní pro aplikaci Human Resources. Vyrostl z platformy Dynamics 365 XRM, která se používá řešeními [Dynamics 365 Customer Engagement](https://docs.microsoft.com/dynamics365/#pivot=business-apps&panel=customer-engagement).

Common Data Service poskytuje platformu a rozhraní API pro datové entity. Při nasazení Human Resources se připojuje k instanci aplikace Common Data Service. Entity pro data Human Resources, které se nasazují do této instance Common Data Service. Entity a jejich data jsou k dispozici pro libovolnou aplikaci, která se může připojit k dané instanci Common Data Service. Human Resources synchronizuje data do a z entit Common Data Service.

Pokud jsou datové entity vyžadované vašimi integračními aplikacemi v Common Data Service, můžete plně využít [Common Data Service a rozhraní API, které podporuje](https://docs.microsoft.com/powerapps/#pivot=home&panel=developer). Mezi podporovaná rozhraní API patří [Dynamics 365 Web API](https://docs.microsoft.com/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), které poskytuje implementaci OData pro přístup k datům služby Common Data Service.

Entity služby Common Data Service a přidružená rozhraní API jsou nejlepší možností pro přístup k datům aplikací Human Resources prostřednictvím webových aplikací, webových služeb / rozhraní API a libovolné další aplikace, která se připojuje ke kanálům OData.

> [!NOTE]
> Vzhledem k tomu, že rozhodnutí učinit ze služby Common Data Service preferované datové rozhraní pro aplikace Human Resources bylo učiněno poměrně nedávno, můžete zjistit, že datové entity aplikací Human Resources, které potřebujete pro vaši integraci, dosud nejsou ve službě Common Data Service přítomné.
</br>
> Pro seznam entit aplikací Human Resources, které jsou k dispozici ve službě Common Data Service, viz [Human Resources a Common Data Service](https://docs.microsoft.com/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Pokud entity aplikací Human Resources nezbytné pro integraci nejsou dosud k dispozici, budete muset počkat na zpřístupnění těchto datových entit nebo použít některou z dalších integračních technologií, které jsou popsány níže.
> </br>
> Ve výchozím nastavení je integrace pomocí služby Common Data Service v nových prostředích, která neobsahují poskytnutá ukázková data, zakázána. U nových prostředí obsahujících ukázková data je tato integrace zapnutá a tato prostředí začínají synchronizovat data, jakmile jsou poskytnuta. Jakmile je vaše prostředí připraveno k synchronizaci dat, můžete spustit integraci.

### <a name="dmfdixf-entities"></a>Entity DMF/DIXF

Human Resources, postavené převážně na stejné platformě jako aplikace Finance and Operations, poskytují [Data Management Framework (DMF)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json). DMF je také znám jako Data Import Export Framework (DIXF). Modul Human Resources poskytuje sadu datových entit, které lze použít pro import a export dat Human Resources. Zatímco entity služby Common Data Service jsou preferovaným rozhraním integrace dat pro aplikaci Human Resources, entity DMF jsou nadále za určitých okolností užitečné. Jedná se například o tyto případy:

- Entity služby Common Data Service dosud nejsou k dispozici.

- Integrace vyžaduje funkce pro hromadný import a export dat s vysokým výkonem.

Entity DMF aktuálně poskytují nejúplnější pokrytí pro data aplikace Human Resources.

DMF není vhodné pro integraci v reálném čase, například v případě, kdy potřebujete okamžitou zpětnou vazbu uživatele v uživatelském rozhraní aplikace. Operace balíku jsou naplánovány dávkovou úlohou a často mají minimální hodnotu čekací doby 1-2 před tím, než dávková služba vybere úlohu k provedení, a dále je nutné provést operaci importu nebo exportu.

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

DMF dále poskytuje výkonnou funkci (známou jako [dodejte svou vlastní databázi](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) nebo BYOD), která umožňuje aplikacím Human Resources exportovat data do vaší vlastní SQL databáze Microsoft Azure. Tato funkce poskytuje ohromnou flexibilitu. V případě přítomnosti dat ve vaší vlastní SQL databázi můžete využívat libovolné aplikace nebo middleware, které se mohou připojit k úložišti dat SQL.

BYOD je převážně pouze pro čtení. I když můžete manipulovat s libovolnými daty v SQL databázi Azure a ukládat je (například kombinacemi více datových zdrojů), data uložená v SQL databázi Azure nejsou synchronizována s aplikacemi Human Resources.

BYOD je vhodné pro řešení vykazování, integraci dat a kombinace více datových zdrojů jako datového zdroje pro pipeline [Azure Data Factory.](https://docs.microsoft.com/azure/data-factory/).

> [!NOTE]
> BYOD není k dispozici pro aplikaci Attract a Onboard.

### <a name="odata-enabled-entities"></a>Entity s povolenou službou OData

Většina entit DMF je také povolena pro přístup prostřednictvím datové služby (OData) aplikací Human Resources. Dokumentace, která je poskytována pro [službu OData Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata), se vztahuje na Human Resources s výjimkou vytváření vlastních entit vystavených OData.

I když je služba Common Data Service a implementace služby OData poskytovaná službou Common Data Service (prostřednictvím [Dynamics 365 Web API](https://docs.microsoft.com/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) preferována před datovou službou aplikace Human Resources, datová služba aplikace Human Resources má momentálně úplnější pokrytí entit pro data aplikace Human Resources.

### <a name="excel-add-in"></a>Doplněk pro aplikaci Excel

[Doplněk pro aplikaci Excel](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=/dynamics365/unified-operations/talent/toc.json) využívá entity s povolenou službou OData pod povrchem. Umožňuje koncovému uživateli snadno načíst a upravit data aplikace Human Resources pomocí známého uživatelského rozhraní aplikace Excel.

Doplněk pro aplikaci Excel je vhodný pro ad-hoc importy/exporty dat prováděné odborníky na byznys doménu. Pro opakující se integraci dat, která vyžaduje automatizaci s využitím programu, bude vhodnější další integrační technologie.

### <a name="data-integrator"></a>Služba Data Integrator

Můžete použít [službu Data Integrato](https://docs.microsoft.com/powerapps/administrator/data-integrator) k integraci dat do a z Common Data Service. Službu Data Integrator umožňuje definovat integrační projekty, často na základě předdefinovaných šablon, které vývojáři aplikací přizpůsobili pro konkrétní integrace. Projekty integrace můžete naplánovat tak, aby se spouštěly automaticky na základě opakujícího se harmonogramu, nebo mohou být spouštěny ručně.

Projekty Data Integrator jsou vhodné pro dávkové integrace Common Data Service. Jedná se o skvělou volbu pro integraci mezi aplikací řady Dynamics 365. Například společnost Microsoft poskytuje šablonu služby Data Integrator k integraci dat z aplikace Human Resources do aplikace Dynamics 365 Finance. Další informace o šabloně v [integraci z Dynamics 365 Human Resources do Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Služba Data Integrator podporuje [nástroj Power Query](https://docs.microsoft.com/power-query/power-query-what-is-power-query) prostřednictvím své [funkce Advanced Query](https://docs.microsoft.com/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query poskytuje výkonné, flexibilní filtrování a transformaci dat včetně bohatého jazyka M formula language. Power Query bude pravděpodobně dobře znám v případě, že jste vytvořili sestavy Power BI.

## <a name="deciding-on-an-integration-technology"></a>Rozhodování o technologii integrace

V případě, že je k dispozici mnoho různých integračních technologií, může být rozhodování o volbě přístupu k integraci někdy velmi intenzivní. S rozvojem datového pokrytí ve službě Common Data Service, se bude rozhodování neustále ulehčovat, přičemž služba Common Data Service bude ve většině případů preferované datové rozhraní. Avšak do té doby můžete zjistit, že služba Common Data Service dosud nesplňuje vaše potřeby. Následující tabulka obsahuje souhrn některých hlavních charakteristik možností integračních technologií.

| Technologie / nástroj / rozhraní API    | Opakované integrace                   | Synchronní/asynchronní                    | Programový přístup prostřednictvím rozhraní API        | Vhodné datové objemy                                   | Datové pokrytí                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Entity služby Common Data Service           | Ano, pomocí služby Data Integrator nebo middlewaru | Synch. asynch., dávkově (prostřednictvím služby Data Integrator) | Ano, prostřednictvím Dynamics 365 Web API (OData) | Liší se podle jednotlivých případů použití (podporuje stránkování v případě interaktivního použití) | Vylepšení<sup>2</sup>                       |
| Entity DMF           | Ano, plánováno prostřednictvím middlewaru        | Asynch., dávka                                | Ano, prostřednictvím rozhraní REST API balíčku DMF         | Vysoké (stovky tisíc záznamů)                    | Vysoké                                |
| Rozhraní REST API balíčku DMF   | Ano, plánováno prostřednictvím middlewaru        | Asynch., dávka                                | Ano                                       | Vysoké (stovky tisíc záznamů)                    | Rozhraní API podporuje všechny entity DMF.       |
| BYOD                   | Ano, plánováno správcem v aplikaci Human Resources        | Asynch., dávka                                | Ne<sup>3</sup>                                    | Vysoké (stovky tisíc záznamů)                    | Podporuje všechny entity DMF.           |
| Entity s povolenou službou OData | Ano, použití middlewaru                    | Synchronizovat                                        | Ano, prostřednictvím datové služby (OData) aplikace Human Resources  | Liší se podle jednotlivých případů použití (podporuje stránkování v případě interaktivního použití) | Vysoké                                |
| Doplněk pro aplikaci Excel           | Ne                                       | Synchronizovat                                        | Ne                                        | Střední (desítky tisíc záznamů)                      | Podporuje všechny entity s povolenou službou OData. |
| Služba Data Integrator        | Ano, plánováno ve službě Data Integrator        | Asynch., dávka                                | Ne                                        | Liší se podle případu použití.                                       | Podporuje všechny entity služby Common Data Service.           |

<sup>2</sup>společnost Microsoft intenzivně investuje do zvýšení pokrytí dat pro entity Common Data Service. Doporučujeme použít Common Data Service, pokud je k dispozici pokrytí. Služba Common Data Service poskytuje v současné době nízké datové pokrytí ve srovnánís DMF a entitami s povolenou službou OData.

<sup>3</sup>SQL databáze je přístupná prostřednictvím programu.
