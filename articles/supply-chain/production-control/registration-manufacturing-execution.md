---
title: Registrace pro provádění výroby
description: Toto téma popisuje klíčové pojmy a termíny, které je třeba pochopit ke konfiguraci a používání provádění výroby.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c843bc87c7b9c0676211c8f3363ec3e05ee97d20b3eedc940b9ffaee2d3211fa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718893"
---
# <a name="registration-for-manufacturing-execution"></a>Registrace pro provádění výroby

[!include [banner](../includes/banner.md)]

Toto téma popisuje klíčové pojmy a termíny, které je třeba pochopit ke konfiguraci a používání provádění výroby. 

Provádění výroby je určeno především pro výrobní společnosti. Zaměstnanci mohou registrovat čas a spotřebu zboží ve výrobních úlohách pomocí stránky **Registrace úlohy**. Všechny registrace jsou schváleny a následně převedeny do příslušných modulů . Souvislá schvalování a převod registrací umožňuje správcům snadno sledovat skutečné náklady pro výrobní zakázky.

## <a name="manufacturing-execution-and-registration-terminology"></a>Výrobní výrazy a terminologie registrace
Následující tabulka obsahuje podmínky, které se vztahují k provádění výroby a souvisejícím registračním úlohám.

| Termín                          | popis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Provádění výroby       | Funkce, která slouží k registraci času, spotřebě materiálu a nákladů ve výrobních úlohách, projektech a nepřímých aktivitách. Registrace je prováděna u klienta registrace provádění výroby.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Seznam prací                      | Na stránce **Registrace úlohy** je u zaměstnanců uveden seznam úloh, které je nutné provést prou konkrétních prostředků, jako jsou například stroje. Pracovník může registrovat čas a spotřebu zboží v každé úloze nebo úkolu v seznamu úloh.                                                                                                                                                                                                                                                                                                                                                                           |
| Sdružování úloh                  | Pokud pracovník začne na stránce **Registrace úlohy** více než jednu úlohu současně, jedná se o sdružování úloh. Čas strávený na skupinových úkolech lze přidělit jednotlivým úkolům různými způsoby za pomoci alokačních klíčů.                                                                                                                                                                                                                                                                                                                                                         |
| Registrace vedoucího týmu a asistenta | Pracovník se může u prostředku zaregistrovat jako asistent a vytvořit malý tým, ve kterém spolupracujete několik pracovníků na stejných výrobních úlohách. Zdrojů, ke kterým jsou zaměstnanci připojeni jako asistenti, se nazývají vedoucí prostředky. Pouze pro vedoucí prostředky se musí provádět registrace. Všem asistentům je automaticky přidělena stejná registrace. Pokud je například jako vedoucí prostředek určen stroj, pracovník, který je registrován jako asistent stroje, může provádět registrace na stránce **Registrace úlohy** a stroj i pracovníci připojeni jako asistenti obdrží totožnou registraci. |
| Nepřímá aktivita             | Aktivity nebo úlohy, které přímo nesouvisí s výrobní úlohou nebo projektem, jako například schůzka oddělení, úklid nebo údržba v dílně. Zaměstnanci mohou provádět registraci nepřímých aktivit stejným způsobem, jako při registraci výrobních úloh a projektů.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Registrace při spouštění výroby
Zaměstnanci mohou provádět různé typy registrací spuštění výroby v rámci produkčních úloh výroby. V závislosti na nastavení systému je možné také provádět registrace aktivit projektu a neproduktivních úloh, jako jsou například přestávky, absence a nepřímé aktivity. Zde jsou typy registrace:

-   **Příchod/odchod** (k dispozici s časem a docházkou) – zaměstnanci označí příchod při příchodu do práce a odchod po skončení a odchodu domů.
-   **Registrace výrobní úloh** – Pracovníci mohou provádět registrace, jako je například zahájení úlohy a hlášení zpětné vazby o výrobních úlohách, které jsou zobrazeny v jeho seznamu úloh. Pracovníci mohou spustit několik úloh najednou. Tento postup se nazývá sdružování úloh.
-   **Registrace zásob** – Pracovníci mohou provádět registraci materiálů použitých v dílně, které přímo nesouvisejí s výrobními úlohami. Příklady: maziva nebo jiný materiál používaný pro řádný chod strojů. Registrace probíhá v deníku zásob.
-   **Registrace na projektech** (k dispozici s časem a docházkou) – pracovníci mohou provádět registrace, jako je například zahájení nebo dokončení práce u projektů nebo aktivit projektu, které jsou zobrazeny v seznamu úloh.
-   **Registrace poplatků za projekt a položky projektu** (k dispozici s časem a docházkou) – zaměstnanci mohou registrovat poplatky (výdaje), které jsou přidruženy k projektu, do deníku poplatků projektu, jako je například poplatek za míli a přejezd mostu. Zaměstnanci mohou registrovat také spotřebu položky v projektech. To se provádí v deníku položek projektu.
-   **Registrace jako asistent jiného pracovníka** – Jestliže dvě nebo více zaměstnanců budou spolupracovat na výrobní úloze nebo projektu, pracovník se může registrovat jako asistent stroje, nebo jiného pracovníka, který bude mít funkci vedoucího. V případě potřeby může vedoucí vybrat jiného pracovníka na místo vedoucího.
-   **Registrace absence** (k dispozici s časem a docházkou) – zaměstnanci mohou registrovat čas u různých kódů absencí, které jsou nastaveny. Absenci je možné označit v případě, že pracovník přijde pozdě, vyžaduje absenci během pracovního dne nebo opustí pracoviště dříve, než bylo očekáváno podle standardního profilu pracovní doby.
-   **Záznam přestávek** (k dispozici s časem a docházkou) – během pracovního dne zaměstnanci mohou registrovat, své opuštění pracovní stanici kvůli přestávce. Můžete nastavit několik typů přestávky. Když se pracovník vrátí a přihlásí se znovu, systém zaregistruje že pracovník je zpět a zastaví registraci přestávky.
-   **Registrace nepřímých aktivit** (k dispozici s časem a docházkou) – nepřímé aktivity jsou nevýrobní aktivity, kterých se mohou zaměstnanci účastnit během pracovního dne, jako například schůzky oddělení, schůzky týmu nebo úloha údržby, která se provádí v dílně. Zaměstnanci mohou provádět registraci nepřímých aktivit, které jsou nastaveny.
-   **Registrace přesčasu** (k dispozici s časem a docházkou) – pracovníci, kteří byli požádáni o delší pracovní dobu, mohou určit, zda by další hodiny měly být registrovány s pružnou pracovní dobou nebo jako placený přesčas.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]