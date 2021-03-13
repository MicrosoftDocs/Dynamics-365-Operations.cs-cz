---
title: Odebrané nebo zastaralé funkce platformy
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy aplikací Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: d57182aa34c4897ef3703d0f8ed08d032c261170
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154080"
---
# <a name="removed-or-deprecated-platform-features"></a>Odebrané nebo zastaralé funkce platformy

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy aplikací Finance and Operations.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://docs.microsoft.com/dynamics/s-e/). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.

## <a name="feature-removed-effective-january-28-2021"></a>Funkce odstraněna s účinností od 28. ledna 2021

### <a name="batch-job-to-handle-sql-index-defragmentation"></a>Dávková úloha pro zpracování defragmentace SQL indexu

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Abychom snížili režii provozu, monitorování a údržby správy indexu zákazníky, byla tato funkce odstraněna. |
| **Nahrazeno jinou funkcí?**   | Do budoucna budou údržbu indexu provádět služby společnosti Microsoft. K tomu bude docházet nepřetržitě, aniž by to ovlivnilo pracovní vytížení uživatele. |
| **Ovlivněné oblasti produktu**         | Aplikace Finance and Operations|
| **Možnost nasazení**              | Nasazení v cloudu - ovlivňuje provozní prostředí spravovaná společností Microsoft a prostředí sandbox Tier 2 až Tier 5. |
| **Stav**                         | Tato funkce byla odstraněna. |


## <a name="platform-updates-for-version-10017-of-finance-and-operations-apps"></a>Aktualizace platformy pro verzi 10.0.17 aplikací Finance and Operations

> [!IMPORTANT]
> Verze 10.0.17 je k dispozici jako součást vydání náhledu. Obsah a funkce se mohou změnit. Další informace o předchozích verzích naleznete v tématu [Často kladené dotazy k aktualizacím služby One Version](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Chcete-li podporovat nejnovější verze Visual Studio, je třeba provést určité změny v rozšířeních X ++ pro Visual Studio. Tyto změny nejsou kompatibilní s Visual Studio 2015. |
| **Nahrazeno jinou funkcí?**   | Visual Studio 2017 nahradí Visual Studio 2015 jako nasazená a požadovaná verze. |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé. Po aktualizaci budou předchozí nástroje X++ odebrány z Visual Studio 2015 a aktualizované nástroje se nebudou instalovat ve Visual Studio 2015. Na hostovaná sestavení to nemá žádný dopad. U sestavování virtuálních počítačů je nutné ručně aktualizovat kanál sestavení (definice sestavení), aby se změnila závislost z MSBuild 14.0 (Visual Studio 2015) na MSBuild 15.0 (Visual Studio 2017), jak je popsáno v části [Aktualizace staršího kanálu v Azure Pipelines](../dev-tools/pipeline-msbuild-update.md). |

### <a name="user-avatar"></a>Uživatelský avatar 

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Avatar uživatele, který se zobrazuje na pravé straně navigačního panelu, byl načten pomocí rozhraní API z ovládacího prvku záhlaví Dynamics 365, jehož podpora byla ukončena. |
| **Nahrazeno jinou funkcí?**   | Uživatelé místo toho uvidí své iniciály v kruhu na navigačním panelu. Toto je stejný vizuál, jaký se aktuálně používá na vývojových počítačích. |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Odstraněno od verze 10.0.17. |

### <a name="enterprise-portal-ep-deprecation"></a>Ukončení podpory portálu Enterprise (EP)  

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Artefakty metadat spojené s Dynamics AX 2012 Enterprise Portal (EP) byly vyřazeny, protože aplikace Finance and Operations nikdy nepodporovaly EP. |
| **Nahrazeno jinou funkcí?**   | Žádný |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Zastaralé. Ve vydání z října 2021 je naplánováno odstranění všech kódů EP. |

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Aktualizace platformy pro verzi 10.0.15 aplikací Finance and Operations

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Podpora aplikace Internet Explorer 11 pro Dynamics 365 je zastaralá

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | S platností od prosince 2020 je podpora aplikace Microsoft Internet Explorer 11 zastaralá pro všechny produkty Dynamics 365 a Internet Explorer 11 nebude podporován po srpnu 2021.<br><br>To bude mít dopad na zákazníky, kteří používají produkty Dynamics 365, které jsou navrženy pro použití prostřednictvím rozhraní Internet Explorer 11. Po srpnu 2021 nebude Internet Explorer 11 podporován pro takové produkty Dynamics 365. |
| **Nahrazeno jinou funkcí?**   | Doporučujeme zákazníkům přejít na Microsoft Edge.|
| **Ovlivněné oblasti produktu**         | Všechny produkty Dynamics 365 |
| **Možnost nasazení**              | Vše|
| **Stav**                         | Zastaralé. Internet Explorer 11 nebude podporován po srpnu 2021.|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Doplněk sady Visual Studio pro použití oprav hotfix metadat

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Opravy hotfix metadat už nejsou podporovány u aktualizací služeb [One Version](../../fin-ops/get-started/one-version.md), které byly zavedeny v červenci 2018 s verzí 8.1. |
| **Nahrazeno jinou funkcí?**   | Pro podporované verze nejsou k dispozici jednotlivé opravy hotfix metadat. Místo toho se použijí kumulativní aktualizace pro zvýšení kvality. |
| **Ovlivněné oblasti produktu**         | Doplňky sady Visual Studio |
| **Možnost nasazení**              | Virtuální počítae pro vývoj |
| **Stav**                         | Od verzei 10.0.15 už tento doplněk není součástí nástrojů sady Visual Studio. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Aktualizace platformy pro verzi 10.0.14 aplikací Finance and Operations

### <a name="online-users-page"></a>Stránka online uživatelů 

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Toto je starší stránka, která byla vytvořena pro předchozí architekturu klient/server. Informace na této stránce nejsou vždy přesné, což může být matoucí a zavádějící. |
| **Nahrazeno jinou funkcí?**   | V budoucí aktualizaci poskytneme novou stránku.|
| **Ovlivněné oblasti produktu**         | Správa systému |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Do října 2021 bude tento formulář odstraněn.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Aktualizace platformy pro verzi 10.0.13 aplikací Finance and Operations


### <a name="custom-code-defined-in-ssrs-report-properties"></a>Vlastní kód definovaný ve vlastnostech sestavy SSRS 

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Obecně lze říci, že vlastní kód nabízí omezené výhody a zároveň vyžaduje značné zdroje a podporu pro výpočet. Vlastní kód je primárně používán autory sestav k volání veřejných metod z vlastní sestavy kódu. Služba hostovaná v cloudu však nepodporuje odkazy na vlastní sestavení pro zprávy SSRS. |
| **Nahrazeno jinou funkcí?**   | Autoři sestav se mohou rozhodnout pokračovat v odkazování na veřejná rozhraní .NET API pro operace Math, Převod a Formát z libovolného výrazu textového pole. Další informace naleznete v tématu [Přidání kódu do sestavy (SSRS)](https://docs.microsoft.comsql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15).  |
| **Ovlivněné oblasti produktu**         | Podmnožina návrhů sestav aplikací definovaných v RDL, kterě obsahují vlastní kód. |
| **Možnost nasazení**              | Vše |
| **Stav**                         | U verzí novějších než 10.0.13 kompilátor začne vydávat varování pro případy, kdy je v definici sestavy SSRS detekován vlastní kód. Chcete-li problém vyřešit, otevřete definici návrhu sestavy a odeberte všechny artefakty vlastního kódu. Toto varování bude v budoucí aktualizaci nahrazeno chybou kompilátoru.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Upgrade tří knihoven komponent jQuery 

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Jsou aktualizovány tři knihovny komponent jQuery pro opravy zabezpečení a udržování měny.   
| **Nahrazeno jinou funkcí?**   | Ovlivněny jsou následující knihovny: jQuery (do verze 3.5.0 od verze 2.1.4), jQuery UI (do verze 1.12.1 od verze 1.11.4), jQuery qTip (do verze 3.0.3 od verze 2.2.1). Pokyny pro migraci poskytuje online jQuery.  |
| **Ovlivněné oblasti produktu**         | Rozšiřitelné ovládací prvky, konkrétně vlastní kód JavaScript využívající zastaralá nebo odstraněná rozhraní API. |
| **Možnost nasazení**              | Vše |
| **Stav**                         | V aktualzaci 10.0.13/Platform update 37 mohou zákazníci volitelně přecházet k nejnovějším knihovnám povolením funkce Upgradovat tři knihovny komponent jQuery. Přechod na nové knihovny bude povinný s vydáním z dubna 2021, aby byl k dispozici čas na migraci příslušných rozhraní API.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Existující API pro ovládací prvek mřížky / forceLegacyGrid ()

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Stávající ovládací prvek mřížky se nahrazuje novým ovládacím prvkem mřížky. |
| **Nahrazeno jinou funkcí?**   | [Nový ovládací prvek mřížky](../..//fin-ops/get-started/grid-capabilities.md) |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Ve verzi 10.0.13 je nový ovládací prvek mřížky obecně k dispozici a zákazníci mohou tuto funkci volitelně zapnout. Nový ovládací prvek mřížky začne být povinný od vydání z října 2021. Jakmile bude nový ovládací prvek mřížky povinný, rozhraní API **forceLegacyGrid()** přestane být respektováno. |

### <a name="personalization-without-saved-views"></a>Přizpůsobení bez uložených pohledů 

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Podsystém personalizace byl přepracován funkcí uložených pohledů, takže má lepší výkon a nabízí další možnosti. |
| **Nahrazeno jinou funkcí?**   | Uložená zobrazení |
| **Ovlivněné oblasti produktu**         | Webový klient |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Ve verzi 10.0.13 / Platform Update 37 je funkce uložených pohledů obecně k dispozici a zákazníci ji mohou volitelně zapnout. Funkce uložených pohledů začne být povinný od vydání z října 2021. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Aktualizace platformy pro verzi 10.0.12 aplikací Finance and Operations

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Rozšíření formuláře ovládacího prvku mřížky nebo skupiny obsahující neplatné odkazy na pole

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Vlastnost datové skupiny v mřížce nebo skupinových ovládacích prvcích se používá k automatickému zobrazení všech polí skupiny polí. Ovládací prvek mřížky nebo skupiny přidaný pomocí rozšíření může obsahovat pole, která již nejsou definována ve skupině polí, nebo to mohou být chybějící pole, která jsou definována ve skupině polí. To může způsobit nekonzistentní chování za běhu. Aktualizace platformy pro verze 10.0.12 aplikací Finance and Operations nyní kategorizují tento problém jako *varování* kompilátoru. Chcete-li tento problém vyřešit, otevřete rozšíření formuláře a uložte je.
| **Nahrazeno jinou funkcí?**   | Toto varování kompilátoru bude v budoucí aktualizaci nahrazeno chybou kompilátoru. |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Varování kompilátoru je chybou kompilátoru v aktualizacích platformy pro verze 10.0.12 aplikací Finance and Operations. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Aktualizace platformy pro verzi 10.0.11 aplikací Finance and Operations

### <a name="explicit-safe-lists-for-self-service-environments"></a>Explicitní bezpečné seznamy pro samoobslužná prostředí

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Proces přesunu IP do bezpečných seznamů se změnil. Samoobsluha již nepodporuje bezpečné seznamy IP. |
| **Nahrazeno jinou funkcí?**   | Další informace získáte v tématu [Konfigurace podmíněného přístupu Azure Active Directory](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Ovlivněné oblasti produktu**         | Zabezpečení |
| **Možnost nasazení**              | Cloud |
| **Stav**                         | **Zastaralé:** Tato funkce je plně zastaralá pro samoobslužná nasazení. |

### <a name="visual-studio-2015"></a>Visual Studio2015

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Chcete-li podporovat nejnovější verze Visual Studio, je třeba provést určité změny v rozšířeních X ++ pro Visual Studio. Tyto změny nejsou kompatibilní s Visual Studio 2015. |
| **Nahrazeno jinou funkcí?**   | Visual Studio 2017 nahradí Visual Studio 2015 jako nasazená a požadovaná verze. |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Virtuální počítače nasazené na verzi 10.0.13 (Platform update 37) nebo novější obsahují Visual Studio 2017. Verze 10.0.16 (Platform update 40) je finální vydání s podporou pro Visual Studio 2015. Virtuální stroje pouze s verzí Visual Studio 2015 nebude možné aktualizovat na verzi 10.0.17 (Platform update 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Skupiny polí obsahující neplatné odkazy na pole

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Skupiny polí v definicích metadat tabulky mohou obsahovat odkazy na pole, které nejsou platné. Při nasazení těchto skupin polí to může způsobit chyby runtime ve Financial Reporting a Microsoft SQL Server Reporting Services (SSRS). Aktualizace platformy 23 zavedla *upozornění* kompilátoru, které umožnilo adresovat tento problém s metadaty. Aktualizace platformy pro verze 10.0.11 aplikací Finance and Operations kategorizují tento problém jako *chybu* kompilátoru.<p>Chcete-li opravit problém, postupujte následovně.</p><ol><li>Odeberte neplatný odkaz na pole z definice skupiny pole tabulky.</li><li>Překompilujte.</li><li>Zkontrolujte, zda jsou řešeny všechny chyby.</li></ol> |
| **Nahrazeno jinou funkcí?**   | Tato chyba kompilátoru trvale nahrazuje upozornění kompilátoru.  |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | **Zastaralé:** upozornění kompilátoru je chybou kompilátoru v aktualizacích platformy pro verze 10.0.11 aplikací Finance and Operations. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>Licence ISV vytvořené pomocí algoritmu hash SHA1

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Proces vytvoření licencí nezávislého softwaru dodavatele (ISV) se změnil. Další informace naleznete v tématu [Správa licencí nezávislého dodavatele softwaru (ISV)](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Nahrazeno jinou funkcí?**   | Ano. Vytvoření licencí pomocí prostředí Windows PowerShell. |
| **Ovlivněné oblasti produktu**         | Vývojové nástroje Visual Studio |
| **Možnost nasazení**              | Vše |
| **Stav**                         | <strong>Zastaralé:</strong> licence ISV, které byly vytvořeny pomocí algoritmu hash SHA1. Tento algoritmus závisí na certifikátech, které byly vytvořeny pomocí nástroje MakeCert, a tento nástroj se již nepoužívá.<p><strong>Zastaralé:</strong> použití algoritmu SHA1 pro účely zabezpečení nebo vytřídění. Algoritmus SHA1 přestane fungovat v na začátku roku 2021. Proto by již neměl být používán.<p><strong>Odebráno:</strong> podpora pro příchozí nebo odchozí požadavky zabezpečení TLS 1.0 a TLS 1.1. |

## <a name="platform-update-32"></a>Platform update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogové okno pro změnu požadavku workflowu již neobsahuje rozevírací seznam pro výběr uživatele.
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Jednalo se o bezpečnostní problém, protože požadavek na změnu mohl být odeslán nežádoucímu uživateli. Šlo také o problém s využitelností, protože aplikace nutila uživatele určit, kdo je původce workflowu, a ručně jej vybrat.  |
| **Nahrazeno jinou funkcí?**   | Ne |
| **Ovlivněné oblasti produktu**         | Workflow |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Rozevírací seznam pro výběr uživatelů byl odebrán z dialogového okna pro změnu požadavku v aktualizaci platformy 32. Požadavky na změnu požadavku budou automaticky odeslány původci, jak bylo zamýšleno. Další informace o této funkci naleznete v tématu [Akce v procesech schválení workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Vložené odkazy na procházení k podrobnostem již nejsou podporovány ve stránkovaných dokumentech vykreslených službou hostovanou v cloudu 
|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Adresy URL pro navigaci vložené do dokumentů vykreslených službou mohou obsahovat citlivé obchodní údaje. Odebíráme podporu vložených odkazů na procházení k podrobnostem coby bezpečnostní opatření pro další ochranu dat zákazníka. V důsledku této změny si uživatelé také užijí lepšího výkonu při interaktivním vytváření dokumentů.  |
| **Nahrazeno jinou funkcí?**   | Žádný |
| **Ovlivněné oblasti produktu**         | Vykazování |
| **Možnost nasazení**              | Vše |
| **Stav**                         | Tato funkce je aktivně odebírána ze služby.<br><br>Moderní klient nabízí řadu možností pro vytváření zobrazení s automaticky generovanými odkazy, které pomáhají při navigaci v aplikaci. Stránkované dokumenty vykreslené službou jsou doporučeny pro externí sdělení, které jsou zasílány e-mailem, archivovány a vytištěny pro příjemce. Zlepšili jsme prostředí pro zobrazení náhledu dokumentů přímo v prohlížeči, které nabízí přímý přístup k místním tiskárnám. Další informace naleznete v tématu [Náhled dokumentů PDF pomocí integrovaného prohlížeče](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Předchozí oznámení o odebraných nebo zastaralých funkcích
Další informace o funkcích, které byly v předchozích verzích odebrány nebo zastaraly, naleznete v tématu [Odebrané nebo zastaralé funkce v předchozích verzích](../migration-upgrade/deprecated-features.md).

