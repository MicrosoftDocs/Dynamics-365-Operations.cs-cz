---
title: Přímé dodávky
description: V tomto článku jsou informace o přímých dodávkách. Přímé dodávky jsou dodávky odeslané od dodavatele přímo odběrateli.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchCreateFromSalesOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 9704
ms.assetid: 64c51384-8a4e-45d0-83c1-12cea22902f9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4550270e87121db4012c273b63576db113a2fbf1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998521"
---
# <a name="direct-deliveries"></a>Přímé dodávky

[!include [banner](../includes/banner.md)]

V tomto článku jsou informace o přímých dodávkách. Přímé dodávky jsou dodávky odeslané od dodavatele přímo odběrateli.

Přímé dodávky zkracují čas potřebný na doručení a náklady související s uskladněním, protože není nutné produkty držet na skladě před jejich odesláním odběrateli.  

Přímé dodávky můžete vytvářet prostřednictvím stránky **Prodejní objednávka**. Nejprve vytvořte prodejní objednávku a řádky objednávky. Poté v podokně akcí na kartě **Prodejní objednávka** zvolte možnost **Přímá dodávka**. Nakonec zadejte řádky, které mají být zpracovány jako přímé dodání. Mezi řádky prodejní objednávky pro přímé doručení a jejich odpovídajícími protějšky v nákupní objednávce je nyní vytvořeno propojení.  

**Poznámka:** Pokud již byla část objednaného množství dodána, je nutné zbývající množství rozdělit. Vytvořte nový řádek pro množství, které musí být dodáno přímo, a odečtěte toto množství od množství na původním řádku. Pokud například původní množství bylo 15 a pět bylo dodáno, musíte vytvořit nový řádek pro zbývající množství 10 a pak původní množství snížit podle částky.  

Jakmile vytvoříte propojení přímé dodávky mezi řádky prodejní objednávky a řádky nákupní objednávky, můžete aktualizovat prodejní objednávku pomocí dodacího listu. Spusťte buď aktualizaci dodacího listu nebo aktualizaci faktury z nákupní objednávky. Musíte aktualizovat fakturaci formuláře prodejní objednávky na stránce **Prodejní objednávky**. Aktualizace faktury nesmí způsobit, že množství na prodejní objednávce překročí množství, které bylo registrováno jako přijaté. Například řádek prodejní objednávky je 10 kusů, ale pouze pět kusů z řádku prodejní objednávky bylo aktualizováno pomocí dodacího listu. Vyberete-li možnost **Vše** v seznamu **Množství**, při aktualizaci faktury prodejní objednávkou budou na faktuře aktualizovány pouze ty položky, které byly fyzicky přijaty nebo byly aktualizovány pomocí dodacího listu. Nebude aktualizován celý řádek prodejní objednávky.

## <a name="delivery-date"></a>Datum dodání
Při aktualizaci pole **Požadované datum příjmu** v řádku prodejní objednávky se aktualizuje také pole **Datum dodání** v odpovídajícím řádku nákupní objednávky. Podobně také platí, že když aktualizujete pole **Potvrzeno** v řádku nákupní objednávky, aktualizují se také pole **Potvrzené datum příjmu** a **Potvrzené datum expedice** v odpovídajícím řádku prodejní objednávky.

## <a name="delivery-address"></a>Adresa dodání
Adresa dodání pro nákupní objednávku je obvykle adresou společnosti. Při vytvoření přímé objednávky však jako adresu dodání zadáváte adresa odběratele. Pokud upravíte adresu dodání pro řádek nákupní objednávky, který má typ **Přímá dodávka**, dojde také k aktualizaci odpovídajícího řádku prodejní objednávky. Pokud obdobně upravíte adresu dodání v řádku prodejní objednávky, nová adresa bude aktualizována také na řádku nákupní objednávky.

## <a name="deleting-order-lines"></a>Odstranění řádků objednávky
Pokud se pokusíte odstranit řádek prodejní objednávky, který má typ dodání **Přímá dodávka**, zobrazí se zpráva s oznámením, že k řádku jsou připojeny řádky nákupní objednávky. Pokud byl řádek prodejní objednávky částečně doručený, nelze odstranit řádek prodejní objednávky ani řádky nákupních objednávek, které jsou k němu přidruženy.

## <a name="warehouse"></a>Sklad
Když vytvoříte přímou dodávku, nebudou prodávané položky nikdy fyzicky přijaty do skladu. Přesto je třeba určit sklad na řádku prodejní objednávky. Obdobě mohou být požadavky na vyskladnění uvedeny ve skupině modelu položky pro položku. Nicméně vzhledem k tomu, že položky nikdy fyzicky nedorazí do skladu, jsou tyto požadavky ignorovány, je-li prodejní objednávka přímou dodávkou.



