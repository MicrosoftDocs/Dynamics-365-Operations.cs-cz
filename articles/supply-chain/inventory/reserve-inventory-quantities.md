---
title: Rezervace skladových množství
description: V tomto článku jsou popsány různé možnosti, které jsou k dispozici pro rezervaci zásob.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 207264
ms.assetid: 47537e4f-cdf6-4813-96fd-c945b2dfe9d4
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0c0e283189998473469164398fa6f43c8e8825e
ms.sourcegitcommit: 3a882de1f1c27654a8e92ebc1999c75678cc9a53
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/27/2022
ms.locfileid: "9201859"
---
# <a name="reserve-inventory-quantities"></a>Rezervace skladových množství

[!include [banner](../includes/banner.md)]

V tomto článku jsou popsány různé možnosti, které jsou k dispozici pro rezervaci zásob.

Na konkrétní prodejní objednávku lze automaticky rezervovat skladové množství. To znamená, že rezervované zásoby nemohou být ze skladu odebrány na jiné objednávky, dokud se nezruší rezervace zásob nebo její část.

Důvodů pro rezervaci zásob je několik:
-   První objednané, první dodané, což znamená, že odběratel obdrží dostupné položky ve stejném pořadí, v jakém objednávky zadával.
-   Nedostatek položek z důvodu dlouhého nebo neznámého času dodání od dodavatele. Je možné, že budete muset zajistit, aby byly jistým odběratelům nebo na jisté objednávky dodány první dostupné položky.
-   Někteří odběratelé a jisté typy objednávek mají při dodání přednost.
-   Položky se sériovými čísly a čísly dávek. Některé položky, které byly nebo budou dodány na určité objednávky, lze označit.
-   Zvláště objednané položky, které jsou rezervovány na určité objednávky.
-   Výrobní zakázky. Můžete například označit položky, které se vyrábí nebo upravují na základě specifických objednávek.

Zásoby lze rezervovat automaticky při vytvoření nového řádku objednávky nebo je lze rezervovat ručně na jednotlivých objednávkách. Dále je možné rezervovat zásoby v různých fázích procesu výroby. Lze rezervovat pouze produkty na skladě. Služby rezervovat nelze, protože pro ně neexistuje dostupné množství. Lze rezervovat jak fyzické množství na skladě, tak objednané, ale ještě nepřijaté zásoby. Pokud se rezervuje větší množství než to, které je obsaženo ve skladovém množství, zobrazí se zpráva, že takto vysoké množství nelze rezervovat. Pak lze buď dané množství přesto rezervovat, nebo je možné objednané množství změnit. Množství lze buď rezervovat, nebo změnit. Pokud se rezervuje větší než dostupné množství, bude nedostatek pokryt tehdy, až budou položky k dispozici pro dodání.

## <a name="inventory-reservation-policies"></a>Zásady rezervace zásob
Zásady rezervace zásob, které jsou nastaveny na stránce **Skupiny modelů položek**, stránce **Parametry řízení zásob a skladu** a stránce **Parametry výroby**.
### <a name="policies-on-the-item-model-groups-page"></a>Zásady na stránce Skupiny modelů položek

Část **Zásady zásob** obsahuje následující zásady rezervace.

| &nbsp;                  | &nbsp;                                                                                                                                     |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Zásada rezervace**  | **Popis**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Řízení FIFO podle data    | Pokud jste vybrali možnost **Řízení FIFO podle data**, rezervace zásob se řídí podle data třídění podle principu FIFO. Dávky jsou rezervovány na základě nejbližšího data příjmu položek podle principu první do skladu, první ze skladu (FIFO).                                                                                                                                                                                                                                                                       |
| Zpět od data expedice | Tato možnost je k dispozici, jen pokud vyberete možnost **Řízení FIFO podle data**. Vyberete-li **Zpět od data expedice**, zásoby se rezervují zpětně od požadovaného data expedice podle principu poslední do skladu, první ze skladu (LIFO). Pokud nejsou k dispozici žádné příjmy před datem expedice, použije se rezervace FIFO.                                                                                                                                                                                                           |
| Rezervace prodeje zboží  | Určuje, zda je rezervace položek ruční nebo automatická. Pokud je rezervace automatická, zásoby se rezervují po vytvoření řádků objednávky. Rezervace je možné porvádět na úrovni čísla položky pro kusovníky (možnost **Automatické**) nebo pro jednotlivé prvky kusovníku (Možnost **Rozpad**). Výchozí hodnota pro **Rezervace prodeje zboží** může být zděděna z **parametrů závazků.** Na této stránce je hodnota nastavena v poli Rezervace v části **Výchozí hodnoty prodeje** **na** kartě **Obecné**. |
| Výběr ze stejné dávky    | Rezervace stejné dávky umožňuje rezervovat zásoby pro řádek prodejní objednávky z jediné dávky zásob. Pokud chcete tuto možnost použít, je nutné nastavit **požadavek na konsolidaci** na **Ano**. Pro sledování skupiny dimenzí skupině a skupiny dimenzí úložiště jsou požadována další nastavení. Další informace naleznete v tématu [Rezervace stejné dávky pro prodejní objednávku](../sales-marketing/reserve-same-batch-sales-order.md).                                                          |
| Požadavek na konsolidaci | Tato možnost je podobná možnosti **Výběr ze stejné dávky** a slučuje zásobu, která je vyhrazena pro řádky prodejní objednávky do jednoho požadavku.                                                                                                                                                                                                                                                                                                                                                                                      |
| Řízení FEFO podle data    | Tato možnost umožňuje rezervaci dávek, které jsou téměř po datu konce platnosti nebo doporučeném datu spotřeby. Je také nutné nastavit hodnotu v poli **Kritéria výběru** a vybrat buď **datum vypršení platnosti** nebo **datum spotřeby**.                                                                                                                                                                                                                                                                                                                              |

#### <a name="example-for-fifo-date-controlled-and-backward-from-ship-date"></a>Příklad pro volby Řízení FIFO podle data a Zpět od data expedice

V tomto příkladu existují zásoby na skladě pro číslo zboží A pro tři různá čísla dávky.

| Č. položky | Číslo dávky | Množství | Datum             |
|-------------|--------------|----------|------------------|
| A.           | 1 000         | 5        | 2. února 2016 |
| A.           | 1 001         | 3        | 1. ledna 2016  |
| A.           | 1 002         | 7        | 3. března 2016    |

Prodejní objednávka, která by měla být automaticky rezervována a dodána 4. dubna 2016, rezervuje následující dávku:
-   Pokud není zaškrtnuté políčko **Řízení FIFO podle data** ani **Zpět od data expedice**, je rezervována dávka 1000, protože se jedná o dávku s nejnižším číslem.
-   Pokud je zaškrtnuto políčko **Řízení FIFO podle data** a není zaškrtnuto políčko **Zpět od data expedice**, je rezervována dávka 1001, protože se jedná o dávku s prvním datem příjmu (FIFO).
-   Pokud je zaškrtnuté políčko **Řízení FIFO podle data** i **Zpět od data expedice**, je rezervována dávka 1002, protože se jedná o dávku nejbližší datu expedice prodejní objednávky.

### <a name="policies-on-the-inventory-and-warehouse-management-parameter-page"></a>Zásady na stránce parametrů Řízení zásob a skladu

Existují dvě možnosti související s rezervacemi na stránce **Parametry řízení zásob a skladu**:
-   Možnost **Rezervovat objednané položky** na kartě **Obecné** umožňuje rezervovat příjmy zboží, které je objednáno proti výdejům položek v oddílech Pohledávky, Řízení a účetnictví projektů a Řízení výroby. Pokud vyberete tuto možnost, budete moci rezervovat položky, které byly fyzicky přijaty. Jestliže byla příslušná položka nastavena pro přijetí záporného skaldu, nebude mít toto pole žádný význam.
-   Možnost **Automatickou rezervovat položky** na kartě **Přeprava** určuje výchozí nastavení, jestliže jsou položky automaticky rezervovány pro převodní příkazy. Výchozí nastavení pro jednotlivé převodní příkazy lze přepsat.

### <a name="inventory-reservation-policies-on-the-production-parameters-page"></a>Zásady rezervace zásob na stránce Parametry výroby

Hodnota pole **Rezervace** na kartě **Obecné** na stránce **Parametry výroby** určuje výchozí místo ve výrobním procesu, kdy se mají rezervovat zásoby. Například zásoby je možné rezervovat při plánování práce nebo při zahájení práce.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
