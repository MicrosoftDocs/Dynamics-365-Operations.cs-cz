---
title: Úvod do pracovních příkazů
description: Toto téma obsahuje přehled pracovních příkazů v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 378fc6d55deada95e94f91ed3f73f2518efbeb1f
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021873"
---
# <a name="introduction-to-work-orders"></a>Úvod do pracovních příkazů

[!include [banner](../../includes/banner.md)]



Pracovní příkazy slouží ke správě, poskytování požadovaných informací a registraci spotřeby pro práce údržby. Každý pracovní příkaz může obsahovat jednu nebo více úloh a lze k němu připojit jednu nebo více položek majetku. Každý řádek pracovního příkazu definuje práce údržby plánované pro majetek.

Pracovní příkazy lze vytvořit následujícími způsoby:

- U plánů údržby založených na kalendáři, kde je zapnuté nastavení Automaticky vytvořit, je to automaticky pomocí příkazu [Naplánovat plány údržby](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md).

- U pořadí údržby založených na kalendáři, kde je zapnuté nastavení Automaticky vytvořit, je to automaticky pomocí příkazu [Naplánovat pořadí údržby](../preventive-and-reactive-maintenance/maintenance-rounds.md).

- U preventivních prací údržby nebo požadavů na údržbu z okna [Rozvrh údržby](../preventive-and-reactive-maintenance/maintenance-schedule.md).

- Ručně

- Ze stránky **Všechny požadavky na údržbu** nebo **Aktivní požadavky na údržbu** nebo **Požadavcích na údržbu v mém funkčním místě**.

>[!NOTE]
>Úlohy pracovního příkazu související se stejným majetkem souvisejí se stejným ID projektu.

## <a name="all-work-orders"></a>Všechny pracovní příkazy

Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** k otevření stránky se seznamem **Všechny pracovní příkazy**. Na této stránce jsou zobrazeny všechny pracovní příkazy a některé související informace.

Na následujícím obrázku je uveden stránky se seznamem **Všechny pracovní příkazy**.

![Obrázek č. 1](media/01-work-orders.png)

Chcete-li zobrazit seznam pouze aktivních pracovních příkazů, vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Aktivní pracovní příkazy**. 

Chcete-li zobrazit seznam úloh pracovního příkazu, které obsahují majetek instalovaný ve funkčních místech, s nimiž souvisíte jako pracovník, vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Moje práce údržby pracovního příkazu funkčního místa**. (Vztah mezi pracovníky a funkčními místy je nastaven na stránce **Pracovníci**. Další informace naleznete v tématu [Pracovníci údržby a skupiny pracovníků](../setup-for-objects/workers-and-worker-groups.md).)

Zde je několik způsobů, jak můžete použít stránku **Všechny pracovní příkazy**:

- V zobrazení mřížky vyberte odkaz ve sloupci **Pracovní příkaz**, chcete-li zobrazit podrobnosti o vybraném záznamu. Poté můžete výběrem možnosti **Upravit** otevřít záznam pro úpravy.

- V zobrazení podrobností jsou uvedeny podrobné informace vztahující se k danému pracovnímu příkazu.  

- Chcete-li zobrazit podrobnosti úlohy pracovního příkazu, v zobrazení podrobností vyberte odkaz **Řádky**, nebo chcete-li zobrazit podrobnosti pracovního příkazu, vyberte odkaz **Záhlaví**.  

- Chcete-li zobrazit další informace související s vybraným pracovním příkazem, rozbalte podokno **související informace** na pravé straně stránky.

Na následujícím obrázku je uveden příklad podrobného zobrazení **Všechny pracovní příkazy**.

![Obrázek č. 2](media/02-work-orders.png)


Tlačítka v podokně akcí jsou uspořádána na kartách. Následující tabulka stručně popisuje tlačítka, která souvisejí se správou majetku:



| Název tlačítka                     | Popis                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Úpravy                            | Úprava vybraného pracovního příkazu.                                                                                                                                                                                                                                           |
| Nové                             | Vytvoření nového pracovního příkazu.                                                                                                                                                                                                                                                  |
| Odstranit                          | Odstranění vybraného pracovního příkazu.                                                                                                                                                                                                                                         |
| Skupina pracovních příkazů                 | Přidání vybraného pracovního příkazu do fondu pracovních příkazů nebo odebrání pracovního příkaz z fondu pracovních příkazů.                                                                                                                                                                                           |
| Upravit                          | Úprava informací o očekávaném počátečním a koncovém datu, úrovni služeb, zodpovědném pracovníkovi údržby nebo zodpovědné skupiny pracovníků údržby na vybraných pracovních příkazech.                                                                                                                                     |
| Související pracovní příkaz              | Vytvoření nového pracovního příkazu souvisejícího s vybranou úlohou pracovního příkazu. To je užitečné v případě, že chcete registrovat primární a sekundární pracovní příkazy.                                                                                                                              |
| Zkopírovat pracovní příkaz                 | Vytvoření nového pracovního příkazu na základě stávajícího pracovního příkazu.                                                                                                                                                                                                               |
| Historická událost                   | Zobrazte historii registrace pro pracovní příkaz.                                                                                                                                                                                                                |
| Poznámky k práci údržby pracovního příkazu                           | Vytvořte popis pracovního příkazu nebo k němu zadejte poznámky. Chcete-li přidat své uživatelské jméno a časové razítko poznámky, začněte kliknutím na tlačítko **Přidat časové razítko**. Poznámky jsou uvedeny na kartě **Popis** na pevné záložce **Podrobnosti o řádku** stránky **Pracovní příkaz**.         |
| Nástroje                           | Vytvoření seznamu požadovaných nástrojů na pracovním příkazu. Nástroje se nastavují jako prostředky v umístění **Správa organizace** > **Prostředky** > **Prostředky**.                                                                                                      |
| Kontrolní seznam údržby           | Zobrazte kontrolní seznam pro majetek připojený k danému pracovnímu příkazu.                                                                                                                                                                                                              |
| Závada majetku                     | Zobrazte nebo registrujte informace o chybě na majetku. Tyto informace se použijí pro správu chyb.                                                                                                                                                                                      |
| Prostoj údržby            | Zadání prostoje údržby pro pracovní příkaz.                                                                                                                                                                                                                               |
| Vyhodnocení stavu            | Registrace měření vyhodnocení stavu na pracovním příkazu.                                                                                                                                                                                                             |
| Čítače majetku                 | Vytvoření nebo zobrazení registrací čítačů pro majetek.                                                                                                                                                                                                                     |
| Prognóza                        | Zobrazení nebo vytvoření prognóz na pracovním příkazu.                                                                                                                                                                                                                               |
| Deníky                        | Zobrazení nebo vytvoření deníků pracovních příkazů. Řádky deníku lze kopírovat z prognóz.                                                                                                                                                                                         |
| Transakce projektu            | Zobrazení všech zaúčtovaných transakcí souvisejících s pracovními příkazy vytvořených pro majetek.                                                                                                                                                                                             |
| Aktualizovat stav pracovního příkazu           | Aktualizujte stav životního cyklu pracovního příkazu.                                                                                                                                                                                                                                                |
| Protokol stavu životního cyklu                      | Zobrazí protokol, který zobrazuje stavy životního cyklu vybraného pracovního příkazu.                                                                                                                                                                                                                   |
| Dokumenty majetku                | Zobrazení seznamu dokumentů připojených k majetku souvisejícím s pracovním příkazem. Tyto dokumenty se nastavují v části **Správa majetku** > **Nastavení** > **Dokumenty majetku**.                                                                                                 |
| Plán                        | Plán vybraných pracovních příkazů.                                                                                                                                                                                                                                      |
| Expedovat            | Plán vybraného pracovního příkazu pro jednoho pracovníka.                                                                                                                                                                                                                        |
| Odstranit plán                 | Odstranění plánování vybraného pracovního příkazu.                                                                                                                                                                                                                          |
| Naplánované práce údržby pracovního příkazu             | Otevře stránku seznamu **Naplánované práce údržby pracovního příkazu**.                                                                                                                                                                                                                             |
| Nákupní žádanka pracovního příkazu | Otevře stránku seznamu **Nákupní žádanka pracovního příkazu**.                                                                                                                                                                                                                 |
| Nákup pracovního příkazu             | Otevře stránku seznamu **Nákupní pracovní příkaz**.                                                                                                                                                                                                                             |
| Řízení nákladů                    | Porovnejte rozpočtové náklady a skutečné náklady na pracovním příkazu.                                                                                                                                                                                                                |
| Řízení hodin                    | Porovnejte prognózované hodiny a skutečné hodiny na pracovním příkazu.                                                                                                                                                                                                                |
| Zpráva pracovního příkazu               | Vytiskněte sestavu pracovního příkazu.                                                                                                                                                                                                                                                |
| Spotřeba pracovního příkazu          | Vytiskněte sestavu spotřeby.                                                                                                                                                                                                                                               |


Tlačítka ve skupině **Projekt** na kartě **Pracovní příkaz** v podokně akcí souvisí s funkcí prognóz, deníků a faktur v modulu **Řízení projektů a účetnictví**.

>[!NOTE]
>Pokud chcete zahrnout prognózy vytvořené v pracovním příkazu při spuštění hlavního plánování pomocí modelu prognózy vybraného na stránce **Parametry správy majetku**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]