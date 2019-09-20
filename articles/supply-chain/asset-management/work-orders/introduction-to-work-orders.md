---
title: Úvod do pracovních příkazů
description: Toto téma obsahuje přehled pracovních příkazů v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9483c50a15fca566b1f5e089297795bbbe09c042
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875554"
---
# <a name="introduction-to-work-orders"></a>Úvod do pracovních příkazů

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Pracovní příkazy slouží ke správě, poskytování požadovaných informací a registraci spotřeby pro práce údržby. Pracovní příkaz může obsahovat jednu nebo více úloh a lze k němu připojit jednu nebo více položek majetku. Každý řádek pracovního příkazu definuje práce údržby plánované pro majetek.

Pracovní příkazy lze vytvořit ručně nebo automaticky:

- Chcete-li automaticky použít formulář **Rozvrhnout plány údržby**, pro plány údržby založené na kalendáři nastavte „Automaticky vytvořit“.  

- Chcete-li automaticky použít formulář **Rozvrhnout pořadí údržby**, pro pořadí údržby založené nastavte „Automaticky vytvořit“.  

- Můžete je vytvořit z rozvrhu údržby, což mohou být preventivní práce údržby nebo požadavky na údržbu.  

- Pracovní příkazy můžete vytvořit ručně.  

- Pracovní příkazy můžete vytvořit v částech **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** nebo **Požadavky na údržbu v mém funkčním místě**.

>[!NOTE]
>Úlohy pracovního příkazu související se stejným majetkem souvisejí se stejným ID projektu.

## <a name="all-work-orders"></a>Všechny pracovní příkazy

Otevřete seznam kliknutím na možnosti **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy**. Seznam **Všechny pracovní příkazy** obsahuje všechny pracovní příkazy a zobrazuje některé informace, které se vztahují k pracovnímu příkazu.

![Obrázek č. 1](media/01-work-orders.png)

- Seznam aktivních pracovních příkazů otevřete kliknutím na možnosti **Správa majetku** > **Společné** > **Pracovní příkazy** > **Aktivní pracovní příkazy**.

- Kliknutím na možnosti **Správa majetku** > **Společné** > **Pracovní příkazy** > **Moje práce údržby pracovního příkazu funkčního místa** zobrazíte seznam úloh pracovních příkazů, které obsahují majetek instalovaný ve funkčních místech, se kterými jako pracovník souvisíte (což je nastaveno v části [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md)).

- V seznamu **Všechny pracovní příkazy** (zobrazení mřížky) klikněte na odkaz ve sloupci **Pracovní příkaz**, chcete-li zobrazit zobrazení podrobností o vybraném záznamu. Klikněte na tlačítko **Upravit**, které chcete otevřít pro úpravy.  

- V zobrazení podrobností jsou uvedeny podrobné informace vztahující se k danému pracovnímu příkazu.  

- Chcete-li zobrazit podrobnosti úlohy pracovního příkazu, v zobrazení podrobností vyberte odkaz **Řádky**, nebo chcete-li zobrazit podrobnosti pracovního příkazu, vyberte odkaz **Záhlaví**.  

- Vertikální podokno **Související informace** napravo od obrazovky obsahuje dodatečné informace o pracovních příkazech. Rozbalením podokna zobrazíte související informace o vybraném pracovním příkazu.  


![Obrázek č. 2](media/02-work-orders.png)


Tlačítka v podokně akcí jsou uspořádána na kartách. Zde je stručný popis tlačítek týkajících se správy podnikového majetku:



| Název tlačítka                     | Popis                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Úpravy                            | Úprava vybraného pracovního příkazu.                                                                                                                                                                                                                                           |
| Nové                             | Vytvoření nového pracovního příkazu.                                                                                                                                                                                                                                                  |
| Odstranit                          | Odstranění vybraného pracovního příkazu.                                                                                                                                                                                                                                         |
| Skupina pracovních příkazů                 | Přidání vybraného pracovního příkazu do fondu pracovních příkazů nebo odebrání pracovního příkaz z fondu pracovních příkazů.                                                                                                                                                                                           |
| Upravit                          | Úprava informací o očekávaném počátečním a koncovém datu, úrovni služeb, zodpovědném pracovníkovi údržby nebo zodpovědné skupiny pracovníků údržby na vybraných pracovních příkazech.                                                                                                                                     |
| Související pracovní příkaz              | Vytvoření nového pracovního příkazu souvisejícího s vybranou úlohou pracovního příkazu. To je užitečné v případě, že chcete registrovat primární a sekundární pracovní příkazy.                                                                                                                              |
| Zkopírovat pracovní příkaz                 | Vytvoření nového pracovního příkazu na základě stávajícího pracovního příkazu.                                                                                                                                                                                                                |
| Historická událost                   | Viz historie registrací na pracovním příkazu.                                                                                                                                                                                                                |
| Poznámky k práci údržby pracovního příkazu                           | Vytvoření popisu nebo vložení poznámek nebo příspěvků do pracovního příkazu. Chcete-li přidat své uživatelské jméno a časové razítko poznámky, začněte kliknutím na tlačítko **Přidat časové razítko**. Poznámky jsou zobrazeny ve formuláři **Pracovní příkaz** > záložka s náhledem **Podrobnosti řádku** > karta **Popis**. |
| Nástroje                           | Vytvoření seznamu požadovaných nástrojů na pracovním příkazu. Nástroje se nastavují jako prostředky v umístění **Správa organizace** > **Společné** > **Prostředky** > **Prostředky**.                                                                                                      |
| Kontrolní seznam údržby           | Zobrazení kontrolního seznamu pro majetek připojený k danému pracovnímu příkazu.                                                                                                                                                                                                              |
| Závada majetku                     | Zobrazení nebo registrace informací o poruše majetku, které se využijí pro správu poruch.                                                                                                                                                                                        |
| Prostoj údržby            | Zadání prostoje údržby pro pracovní příkaz.                                                                                                                                                                                                                               |
| Vyhodnocení stavu            | Registrace měření vyhodnocení stavu na pracovním příkazu.                                                                                                                                                                                                             |
| Čítače majetku                 | Vytvoření nebo zobrazení registrací čítačů pro majetek.                                                                                                                                                                                                                     |
| Prognóza                        | Zobrazení nebo vytvoření prognóz na pracovním příkazu.                                                                                                                                                                                                                               |
| Deníky                        | Zobrazení nebo vytvoření deníků pracovních příkazů. Řádky deníku lze kopírovat z prognóz.                                                                                                                                                                                         |
| Transakce projektu            | Zobrazení všech zaúčtovaných transakcí souvisejících s pracovními příkazy vytvořených pro majetek.                                                                                                                                                                                             |
| Aktualizovat stav pracovního příkazu                | Aktualizace stavu životního cyklu pracovního příkazu.                                                                                                                                                                                                                                                |
| Protokol stavu životního cyklu                       | Protokol zobrazující stavy životního cyklu vybraného pracovního příkazu.                                                                                                                                                                                                                   |
| Dokumenty majetku                | Zobrazení seznamu dokumentů připojených k majetku souvisejícím s pracovním příkazem. Tyto dokumenty se nastavují v části **Správa majetku** > **Nastavení** > **Dokumenty majetku**.                                                                                                 |
| Plán                        | Plán vybraných pracovních příkazů.                                                                                                                                                                                                                                      |
| Expedovat            | Plán vybraného pracovního příkazu pro jednoho pracovníka.                                                                                                                                                                                                                        |
| Odstranit plán                 | Odstranění plánování vybraného pracovního příkazu.                                                                                                                                                                                                                          |
| Naplánované práce údržby pracovního příkazu             | Otevře stránku seznamu **Naplánované práce údržby pracovního příkazu**.                                                                                                                                                                                                                             |
| Nákupní žádanka pracovního příkazu | Otevře stránku seznamu **Nákupní žádanka pracovního příkazu**.                                                                                                                                                                                                                 |
| Nákup pracovního příkazu             | Otevře stránku seznamu **Nákupní pracovní příkaz**.                                                                                                                                                                                                                             |
| Řízení nákladů                    | Porovnejte rozpočtové náklady a skutečné náklady na pracovním příkazu.                                                                                                                                                                                                                |
| Řízení hodin                    | Porovnejte prognózované hodiny a skutečné hodiny na pracovním příkazu.                                                                                                                                                                                                                |
| Zpráva pracovního příkazu               | Tisk sestavy pracovního příkazu.                                                                                                                                                                                                                                                |
| Spotřeba pracovního příkazu          | Tisk sestavy spotřeby.                                                                                                                                                                                                                                               |


Tlačítka na kartě **Pracovní příkaz** > skupina **Projekt** se vztahují k funkcím v modulu **Řízení a účetnictví projektů** týkající se prognóz, deníků a faktur.

>[!NOTE]
>Prognózy vytvořené na pracovním příkazu lze zahrnout při spuštění hlavního plánování pomocí modelu prognózy vybraného ve formuláři **Parametry správy majetku**.
