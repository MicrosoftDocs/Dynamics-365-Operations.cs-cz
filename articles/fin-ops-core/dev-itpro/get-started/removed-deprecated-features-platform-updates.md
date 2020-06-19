---
title: Odebrané nebo zastaralé funkce platformy
description: Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy aplikací Finance and Operations.
author: sericks007
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 6fc699907d30fff2d05e752ea055cae8d1134d9b
ms.sourcegitcommit: 3eaa71c889545318737b3bc88b05eae1a47ad2c0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/05/2020
ms.locfileid: "3433915"
---
# <a name="removed-or-deprecated-platform-features"></a>Odebrané nebo zastaralé funkce platformy

[!include [banner](../includes/banner.md)]

Toto téma popisuje funkce, které byly odebrány nebo u nichž se plánuje odstranění z aktualizací platformy aplikací Finance and Operations.

- *Odstraněná* funkce již není k dispozici v produktu.
- *Zastaralá* funkce není v aktivním nasazení a v budoucí aktualizaci může být odstraněna.

Tento seznam je určen k tomu, aby vám pomohl zvážit tyto odstraněné a zastaralé funkce při svém plánování. 

> [!NOTE]
> Podrobné informace o objektech v aplikacích Finance and Operations lze nalézt v části [Sestavy technických informací](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Můžete srovnat různé verze těchto sestav a zjistíte, které objekty se změnily nebo byly odstraněny v každé z verzí aplikací Finance and Operations.

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

### <a name="explicit-whitelisting-for-self-service-environments"></a>Explicitní whitelisting pro samoobslužná prostředí

|   |  |
|------------|--------------------|
| **Důvod pro zrušení/odstranění** | Proces pro whitelisting IP se změnil. Samoobsluha již nepodporuje whitelisting IP. |
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
| **Stav**                         | Jakmile bude oznámena dostupnost nových virtuálních počítačů (VM) s Visual Studio 2017 ohlášena, stávající VM pouze s Visual Studio 2015 budou muset být znovu nasazeny pomocí vlny vydání 1 z roku 2021. |

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

