---
title: Volba technologie integrace dat
description: Tento článek poskytuje informace o integraci s daty spravovanými v Human resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2c542684642e4f6eda0f862623889a68f85b2b20
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068871"
---
# <a name="choose-a-data-integration-technology"></a>Volba technologie integrace dat


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tento článek obsahuje informace o integraci s daty spravovanými v Dynamics 365 Human Resources. Popisuje různé integrační technologie, které vám pomohou určit, které technologie nejlépe odpovídají vašim potřebám.

## <a name="data-integration-background"></a>Pozadí integrace dat

Obchodní data představují klíčový prostředek, který činí vaši společnost jedinečnou. Data vašeho podniku jsou velice cenná. Vztahy mezi daty, která se shromažďují ve vaší společnosti, můžete použít ke zlepšení obchodních procesů a analytických nástrojů v rámci celé společnosti. Usilujeme o zajištění snadného, zabezpečeného a stabilního přístupu k obchodním datům, ať už se jedná o systém, ze kterého pochází.

V minulosti byla integrace dat mezi více systémy obtížná. Společnost Microsoft činí kroky, které usnadňují integraci dat, a velkým krokem k uskutečnění tohoto cíle je použití služby [Dataverse](/powerapps/maker/common-data-service/data-platform-intro).

Human Resources činí ze služby Dataverse upřednostňované veřejné rozhraní pro data aplikace Human Resources. Očekáváme, že všechna nejdůležitější data spravovaná aplikací Human Resources budou v průběhu času zpřístupněna ve službě Dataverse. Doporučujeme službu Dataverse jako preferovanou technologii pro většinu typů uplatnění v rámci integrace dat.

Uvěodmujeme si, že Dataverse ještě nemusí obsahovat všechna data, která aplikace vyžaduje. Rovněž jsme si uvědomujeme, že časová osa projektu může vyžadovat alternativní technologii. Nezapomeňte nám sdělit, kdy Dataverse nevyhovuje vašim potřebám integrace.

## <a name="integration-technologies"></a>Integrační technologie

V následujících částech jsou popsány různé technologie integrace dat, které jsou k dispozici pro použití s aplikací Human Resources.

### <a name="dataverse-tables"></a>Tabulky Dataverse

Služba Dataverse je preferované veřejné datové rozhraní pro aplikaci Human Resources. Vyrostl z platformy Dynamics 365 XRM, kterou používají řešení [Dynamics 365 Customer Engagement](/dynamics365/?panel=customer-engagement#pivot=business-apps).

Dataverse poskytuje platformu a rozhraní API pro datové tabulky. Při nasazení Human Resources se připojuje k instanci aplikace Dataverse. Entity pro data Human Resources, které se nasazují do této instance Dataverse. Tabulky a jejich data jsou k dispozici pro libovolnou aplikaci, která se může připojit k dané instanci Dataverse. Human Resources synchronizuje data do a z tabulke Dataverse.

> [!NOTE]
> Entity Human Resources odpovídají Dataverse tabulkám. Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Pokud jsou datové tabulky vyžadované vašimi integračními aplikacemi v Dataverse, můžete plně využít [Dataverse a rozhraní API, které podporuje](/powerapps/?panel=developer#pivot=home). Mezi podporovaná rozhraní API patří [Dynamics 365 Web API](/dynamics365/customer-engagement/developer/use-microsoft-dynamics-365-web-api), které poskytuje implementaci OData pro přístup k datům služby Dataverse.

Tabulky služby Dataverse a přidružená rozhraní API jsou nejlepší možností pro přístup k datům aplikací Human Resources prostřednictvím webových aplikací, webových služeb / rozhraní API a libovolné další aplikace, která se připojuje ke kanálům OData.

> [!NOTE]
> Vzhledem k tomu, že rozhodnutí učinit ze služby Dataverse preferované datové rozhraní pro aplikace Human Resources bylo učiněno poměrně nedávno, můžete zjistit, že datové entity aplikací Human Resources, které potřebujete pro vaši integraci, dosud nejsou ve službě Dataverse přítomné.
> </br>
> Pro seznam entit aplikací Human Resources, které jsou k dispozici ve službě Dataverse, viz [Human Resources a Dataverse](/dynamics365/unified-operations/talent/corehrentities).
> </br>
> Pokud entity aplikací Human Resources nezbytné pro integraci nejsou dosud k dispozici, budete muset počkat na zpřístupnění těchto datových entit nebo použít některou z dalších integračních technologií, které jsou popsány níže.
> </br>
> Ve výchozím nastavení je integrace pomocí služby Dataverse v nových prostředích, která neobsahují poskytnutá ukázková data, zakázána. U nových prostředí obsahujících ukázková data je tato integrace zapnutá a tato prostředí začínají synchronizovat data, jakmile jsou poskytnuta. Jakmile je vaše prostředí připraveno k synchronizaci dat, můžete spustit integraci.

### <a name="dmfdixf-entities"></a>Entity DMF/DIXF

Human Resources, postavené převážně na stejné platformě jako finanční a provozní aplikace, poskytují [Data Management Framework (DMF)](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json). DMF je také znám jako Data Import Export Framework (DIXF). Modul Human Resources poskytuje sadu datových entit, které lze použít pro import a export dat Human Resources. Zatímco tabulky služby Dataverse jsou preferovaným rozhraním integrace dat pro aplikaci Human Resources, entity DMF jsou nadále za určitých okolností užitečné. Jedná se například o tyto případy:

- Tabulky služby Dataverse dosud nejsou k dispozici.

- Integrace vyžaduje funkce pro hromadný import a export dat s vysokým výkonem.

> [!NOTE]
> Entity Human Resources odpovídají Dataverse tabulkám. Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Entity DMF aktuálně poskytují nejúplnější pokrytí pro data aplikace Human Resources.

DMF není vhodné pro integraci v reálném čase, například v případě, kdy potřebujete okamžitou zpětnou vazbu uživatele v uživatelském rozhraní aplikace. Operace balíku jsou naplánovány dávkovou úlohou a často mají minimální hodnotu čekací doby 1-2 před tím, než dávková služba vybere úlohu k provedení, a dále je nutné provést operaci importu nebo exportu.

DMF může být nejlepší volbou v případě vysoké požadované propustnosti (například při nočním naplánovaném importu/exportu mnoha tisíc záznamů).

> [!NOTE]
> DMF není k dispozici pro aplikaci Attract a Onboard.

### <a name="dmf-package-rest-api"></a>Rozhraní REST API balíčku DMF

DMF poskytuje rozhraní [REST API](/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api) pro manipulaci s datovými balíčky. Toto rozhraní API lze použít k interakci programu s DMF, jež umožňuje například níže uvedené akce:

- Import datového balíčku.

- Export datového balíčku.

- Kontrola stavu operace importu/exportu.

Rozhraní REST API balíčku DMF je plně podporováno v aplikacích Human Resources.

### <a name="azure-sql-db-byod"></a>Azure SQL DB (BYOD)

DMF dále poskytuje výkonnou funkci (známou jako [dodejte svou vlastní databázi](/dynamics365/unified-operations/dev-itpro/analytics/export-entities-to-your-own-database) nebo BYOD), která umožňuje aplikacím Human Resources exportovat data do vaší vlastní SQL databáze Microsoft Azure. Tato funkce poskytuje ohromnou flexibilitu. V případě přítomnosti dat ve vaší vlastní SQL databázi můžete využívat libovolné aplikace nebo middleware, které se mohou připojit k úložišti dat SQL.

BYOD je převážně pouze pro čtení. I když můžete manipulovat s libovolnými daty v SQL databázi Azure a ukládat je (například kombinacemi více datových zdrojů), data uložená v SQL databázi Azure nejsou synchronizována s aplikacemi Human Resources.

BYOD je vhodné pro řešení vykazování, integraci dat a kombinace více datových zdrojů jako datového zdroje pro pipeline [Azure Data Factory.](/azure/data-factory/).

> [!NOTE]
> BYOD není k dispozici pro aplikaci Attract a Onboard.

### <a name="odata-enabled-entities"></a>Entity s povolenou službou OData

Většina entit DMF je také povolena pro přístup prostřednictvím datové služby (OData) aplikací Human Resources. Dokumentace, která je poskytována pro [službu OData Finance a Operace](/dynamics365/unified-operations/dev-itpro/data-entities/odata), se vztahuje na Human Resources s výjimkou vytváření vlastních entit vystavených OData.

I když je služba Dataverse a implementace služby OData poskytovaná službou Dataverse (prostřednictvím [Dynamics 365 Web API](/previous-versions/dynamicscrm-2016/developers-guide/mt593051(v=crm.8))) preferována před datovou službou aplikace Human Resources, datová služba aplikace Human Resources má momentálně úplnější pokrytí entit pro data aplikace Human Resources.

### <a name="excel-add-in"></a>Doplněk pro aplikaci Excel

[Doplněk pro aplikaci Excel](/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) využívá entity s povolenou službou OData pod povrchem. Umožňuje koncovému uživateli snadno načíst a upravit data aplikace Human Resources pomocí známého uživatelského rozhraní aplikace Excel.

Doplněk pro aplikaci Excel je vhodný pro ad-hoc importy/exporty dat prováděné odborníky na byznys doménu. Pro opakující se integraci dat, která vyžaduje automatizaci s využitím programu, bude vhodnější další integrační technologie.

### <a name="data-integrator"></a>Služba Data Integrator

Můžete použít [službu Data Integrato](/powerapps/administrator/data-integrator) k integraci dat do a z Dataverse. Službu Data Integrator umožňuje definovat integrační projekty, často na základě předdefinovaných šablon, které vývojáři aplikací přizpůsobili pro konkrétní integrace. Projekty integrace můžete naplánovat tak, aby se spouštěly automaticky na základě opakujícího se harmonogramu, nebo mohou být spouštěny ručně.

Projekty Data Integrator jsou vhodné pro dávkové integrace Dataverse. Jedná se o skvělou volbu pro integraci mezi aplikací řady Dynamics 365. Například společnost Microsoft poskytuje šablonu služby Data Integrator k integraci dat z aplikace Human Resources do aplikace Dynamics 365 Finance. Více o šabloně si můžete přečíst v tématu [Integrace z Dynamics 365 Human Resources do Dynamics 365 Finance](hr-admin-integration-finance.md).

### <a name="power-query"></a>Power Query

Služba Data Integrator podporuje nástroj [Power Query](/power-query/power-query-what-is-power-query) prostřednictvím své [funkce Advanced Query](/powerapps/administrator/data-integrator#advanced-data-transformation-and-filtering). Power Query poskytuje výkonné, flexibilní filtrování a transformaci dat včetně bohatého jazyka M formula language. Power Query bude pravděpodobně dobře znám v případě, že jste vytvořili sestavy Power BI.

## <a name="deciding-on-an-integration-technology"></a>Rozhodování o technologii integrace

V případě, že je k dispozici mnoho různých integračních technologií, může být rozhodování o volbě přístupu k integraci někdy velmi intenzivní. S rozvojem datového pokrytí ve službě Dataverse, se bude rozhodování neustále ulehčovat, přičemž služba Dataverse bude ve většině případů preferované datové rozhraní. Avšak do té doby můžete zjistit, že služba Dataverse dosud nesplňuje vaše potřeby. Následující tabulka obsahuje souhrn některých hlavních charakteristik možností integračních technologií.

| Technologie / nástroj / rozhraní API    | Opakované integrace                   | Synchronní/asynchronní                    | Programový přístup prostřednictvím rozhraní API        | Vhodné datové objemy                                   | Datové pokrytí                       |
|------------------------|------------------------------------------|---------------------------------------------|-------------------------------------------|------------------------------------------------------------|-------------------------------------|
| Tabulky Dataverse           | Ano, pomocí služby Data Integrator nebo middlewaru | Synch. asynch., dávkově (prostřednictvím služby Data Integrator) | Ano, prostřednictvím Dynamics 365 Web API (OData) | Liší se podle jednotlivých případů použití (podporuje stránkování v případě interaktivního použití) | Vylepšení<sup>2</sup>                       |
| Entity DMF           | Ano, plánováno prostřednictvím middlewaru        | Asynch., dávka                                | Ano, prostřednictvím rozhraní REST API balíčku DMF         | Vysoké (stovky tisíc záznamů)                    | Vysoké                                |
| Rozhraní REST API balíčku DMF   | Ano, plánováno prostřednictvím middlewaru        | Asynch., dávka                                | Ano                                       | Vysoké (stovky tisíc záznamů)                    | Rozhraní API podporuje všechny entity DMF.       |
| BYOD                   | Ano, plánováno správcem v aplikaci Human Resources        | Asynch., dávka                                | Ne<sup>3</sup>                                    | Vysoké (stovky tisíc záznamů)                    | Podporuje všechny entity DMF.           |
| Entity s povolenou službou OData | Ano, použití middlewaru                    | Synchronizovat                                        | Ano, prostřednictvím datové služby (OData) aplikace Human Resources  | Liší se podle jednotlivých případů použití (podporuje stránkování v případě interaktivního použití) | Vysoké                                |
| Doplněk pro aplikaci Excel           | Ne                                       | Synchronizovat                                        | Ne                                        | Střední (desítky tisíc záznamů)                      | Podporuje všechny entity s povolenou službou OData. |
| Služba Data Integrator        | Ano, plánováno ve službě Data Integrator        | Asynch., dávka                                | Ne                                        | Liší se podle případu použití.                                       | Podporuje všechny Dataverse tabulky           |

<sup>2</sup>společnost Microsoft intenzivně investuje do zvýšení pokrytí dat pro tabulky Dataverse. Doporučujeme použít Dataverse, pokud je k dispozici pokrytí. Služba Dataverse poskytuje v současné době nízké datové pokrytí ve srovnánís DMF a entitami s povolenou službou OData.

<sup>3</sup>SQL databáze je přístupná prostřednictvím programu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

