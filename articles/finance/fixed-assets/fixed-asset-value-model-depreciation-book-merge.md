---
title: Oceňovací model dlouhodobého majetku a slučování knih odpisů
description: V předchozích verzích existovaly dva koncepty ocenění pro dlouhodobý majetek - oceňovací modely a knihy odpisů. Ve vydání Microsoft Dynamics 365 for Operations (1611) byly funkce modelu hodnoty a knihy odpisů sloučeny do jednoho konceptu, který je označován jako kniha.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f027a856dbd596ede84c39e30ee2227aab9329f2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826731"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Oceňovací model dlouhodobého majetku a slučování knih odpisů

[!include [banner](../includes/banner.md)]

V předchozích verzích existovaly dva koncepty ocenění pro dlouhodobý majetek - oceňovací modely a knihy odpisů. Ve vydání Microsoft Dynamics 365 for Operations (1611) byly funkce modelu hodnoty a knihy odpisů sloučeny do jednoho konceptu, který je označován jako kniha.

Funkce nová kniha je založena na dřívější funkcí oceňovacího modelu, ale obsahuje také všechny funkce, které byly dříve k dispozici jen v knihách odpisů. [![Kniha jako sloučení funkce modelu hodnoty a odpisu knihy](./media/fixed-assets.png)](./media/fixed-assets.png) Kvůli tomuto sloučení nyní můžete používat jednu sadu stránek, dotazy a sestavy pro všechny vaše procesy pro dlouhodobý majetek. Tabulky v tomto tématu popisují dřívější funkci pro knihy odpisů a oceňovací modely, spolu s novou funkcí knih.

## <a name="setup"></a>Nastavení
Podle výchozího nastavení se z knih účtuje jak do hlavní knihy (GL), tak do hlavní knihy dlouhodobého majetku. Knihy mají novou možnost **účtovat do hlavní knihy**, která vám umožňuje zakázat zaúčtování do hlavní Knihy a povolit jen zaúčtování do hlavní knihy pro dlouhodobý majetek. Tato funkce se podobá dřívějšímu chování zaúčtování pro knihy odpisů. Nastavení názvů deníků má novou účtovací vrstvu s názvem Žádná. Tato účtovací vrstva byla přidána zejména pro transakce dlouhodobého majetku. K zaúčtování transakcí pro knihy, které nechcete zaúčtovat do hlavní Knihy, je nutné použít název deníku s účtovací vrstvou nastavenou na **Žádná**.

| &nbsp;                                           | Daňové odpisy               | Účetní odpisy                     | (Nová) Kniha                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| Zaúčtovat do hlavní knihy                                   | Nikdy                           | Vždy                          | Možnost pro zaúčtování hlavní Knihy                                |
| Účtovací vrstvy                                   | Nelze použít                  | 3: Stávající, operace a daň | 11: Stávající, operace, daň, 7 vlastních vrstev a Žádná |
| Názvy deníků                                    | Názvy deníku daňových odpisů | Hlavní kniha - Názvy deníků              | Hlavní kniha - Názvy deníků                                      |
| Odvozené knihy                                    | Nepovoleno                     | Povoleno                         | Povoleno                                                 |
| Odpisový plán se přepisuje na úrovni majetku | Povoleno                         | Nepovoleno                     | Povoleno                                                 |

## <a name="processes"></a>Procesy
Procesy nyní využívají běžnou stránku. Některé procesy jsou povoleny pouze v případě, že je možnost **Zaúčtovat do hlavní knihy** nastavena na **č** v nastavení knihy.

| &nbsp;                                           | Daňové odpisy               | Účetní odpisy                     | (Nová) Kniha                                              |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
| Zadání transakce              | Deník daňových odpisů | Deník dlouhodobého majetku | Deník dlouhodobého majetku                      |
| Počáteční mimořádný odpis             | Povoleno                   | Nepovoleno         | Povoleno                                  |
| Odstranit dřívější transakce | Povoleno                   | Nepovoleno         | Povoleno, pouze neúčtujete do hlavní Knihy |
| Hromadná aktualizace                    | Povoleno                   | Nepovoleno         | Povoleno, pouze neúčtujete do hlavní Knihy |

## <a name="inquiries-and-reports"></a>Dotazy a sestavy
Dotazy a sestavy podporují všechny knihy. Sestavy, které nejsou zahrnuty v následující tabulce, dříve podporovaly knihy odpisů a oceňovací modely, a budou i nadále podporovat všechny typy knih. Pole **Účtovací vrstvy** bylo také přidáno do sestav, takže lze snadno identifikovat zaúčtování transakcí.

| &nbsp;                                           | Daňové odpisy               | Účetní odpisy                     | (Nová) Kniha                                              |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
| Dotazy                             | Transakce daňových odpisů | Transakce dlouhodobého majetku | Transakce dlouhodobého majetku |
| Výkaz dlouhodobého majetku                 | Nepovoleno                    | Povoleno                  | Povoleno                  |
| Základ dlouhodobého majetku                     | Povoleno                        | Nepovoleno              | Povoleno                  |
| Použitelnost dlouhodobého majetku v polovině čtvrtletí | Povoleno                        | Nepovoleno              | Povoleno                  |

## <a name="upgrade"></a>Upgradovat
Proces upgradu přesune vaše existující nastavení a všechny vaše existující transakce na novou účetní strukturu. Oceňovací modely zůstanou, jaké momentálně jsou, tedy jako knihy, které se účtují do hlavní knihy. Nicméně, knihy odpisů budou přesunuty do knihy, která má možnost **Zaúčtovat do hlavní knihy** nastavenu na **Ne**. Názvy deníku knihy odpisů bude přesunut do názvu deníku hlavní knihy, který má účtovací vrstvu nastavenou na **Žádná**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]