---
title: Generování řádků faktur při importu faktur dodavatele
description: Toto téma popisuje funkce pro automatické generování řádků faktur na fakturách dodavatele při importu faktur.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e452bda02c814b78c4bb48140b07f0113ab4a571
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358307"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Generování řádků faktur při importu faktur dodavatele

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma popisuje funkce pro automatické generování řádků faktur na fakturách dodavatele při importu faktur.

Někdy faktury dodavatele obsahují omezené informace, jako jsou informace o příjemcích a mezisoučty. Neobsahují však žádné informace o řádkových položkách. Když importujete faktury, budou automaticky generovány řádky faktur na základě informací o odpovídající nákupní objednávce.

Chcete-li povolit automatické vytváření řádků faktury, postupujte takto.

1.  Přejděte do nabídky **Závazky \> Nastavení \> Parametry závazků**.
2.  Na kartě **Automatizace faktur dodavatelů** pod **Automatické vytváření řádků pro importované faktury** nastavte možnost **Automaticky vytvářet řádky faktur** na **Ano**. 
4.  V poli **Vybrat výchozí množství pro automatické vytváření řádků faktur** vyberte množství, které se mají použít k automatickému generování řádků faktur:

    - **Objednané množství** – Řádky budou generovány z řádků nákupní objednávky. Tato hodnota je výchozí hodnota.
    - **Množství příjmu produktu** – Čísla nákupních objednávek se použijí k vyhledání příslušných příjmů produktu. Poté použije množství příjmu produktu ke generování řádků faktury.

## <a name="data-entity-changes"></a>Změny datových entit

Pro podporu funkcí, které jsou popsány v tomto tématu, byla vylepšena datová entita **Záhlaví faktury dodavatele**. Byla přidána tři pole:

- **HeaderOnlyImport** – Toto pole musí být nastaveno na **Ano**, aby byly generovány řádky pro hlavičky faktur.
- **PurchIdRange** – Seznam čísel nákupních objednávek. Čísla faktur mohou být rozsahy, např **INV0001..INV0009** (kde dvě tečky oddělují začátek a konec rozsahu), nebo diskrétní hodnoty, jako např **INV0001, INV0003, INV0006**. Všechny nákupní objednávky musí patřit ke stejnému účtu dodavatele v záhlaví faktury. V opačném případě se zobrazí následující chybová zpráva: „Nepodařilo se vygenerovat řádky faktury. Nákupní objednávky mají různé účty dodavatelů.“
- **PackingslipRange** – Seznam čísel dokladů produktů. Řádky faktury dodavatele lze vytvořit z účtenek produktu. Čísla dokladů produktů však obvykle nejsou na fakturách dodavatele uvedena. Do tohoto pole zadávejte čísla příjemek produktů pouze v případě, že můžete jasně identifikovat příjemky produktů pro které konkrétní faktury. Řádky faktury lze vygenerovat z účtenek produktu. Pokud je toto pole použito, nastavení pole **Vybrat výchozí množství pro automatické vytváření řádků faktur** na stránce **Parametry závazků** je ignorováno. 

**Omezení**: Pokud zadáte více čísel příjemky produktů, vytvoří se několik nevyřízených faktur dodavatele se stejným číslem faktury. Před dalším zpracováním faktury je musíte konsolidovat ručně. V budoucích verzích plánujeme automatickou konsolidaci faktur, takže omezení bude odstraněno.

Všechny příjemky produktů musí patřit ke stejnému účtu dodavatele v záhlaví faktury.

## <a name="result"></a>Výsledek

Pokud se úspěšně vygenerují řádky, do historie automatizace faktur dodavatele se zaprotokoluje následující zpráva: „Automaticky vytvořit řádky faktury: Úspěšně.“

Pokud se generování řádků nezdaří, zaprotokoluje se následující chybová zpráva: „Automaticky vytvořit řádky faktury: Selhalo.“
