## API Report File for "mfc-js"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

// @public (undocumented)
export const BOLD: (children: MfmInline[]) => NodeType<'bold'>;

// @public (undocumented)
export const CENTER: (children: MfmInline[]) => NodeType<'center'>;

// @public (undocumented)
export const CODE_BLOCK: (code: string, lang: string | null) => NodeType<'blockCode'>;

// @public (undocumented)
export const EMOJI_CODE: (name: string) => NodeType<'emojiCode'>;

// @public (undocumented)
export function extract(nodes: MfmNode[], predicate: (node: MfmNode) => boolean): MfmNode[];

// @public (undocumented)
export const FN: (name: string, args: MfmFn['props']['args'], children: MfmFn['children']) => NodeType<'fn'>;

// @public (undocumented)
export const HASHTAG: (value: string) => NodeType<'hashtag'>;

// @public (undocumented)
export const INLINE_CODE: (code: string) => NodeType<'inlineCode'>;

// @public (undocumented)
export function inspect(node: MfmNode, action: (node: MfmNode) => void): void;

// @public (undocumented)
export function inspect(nodes: MfmNode[], action: (node: MfmNode) => void): void;

// @public (undocumented)
export const ITALIC: (children: MfmInline[]) => NodeType<'italic'>;

// @public (undocumented)
export const LINK: (silent: boolean, url: string, children: MfmInline[]) => NodeType<'link'>;

// @public (undocumented)
export const MATH_BLOCK: (formula: string) => NodeType<'mathBlock'>;

// @public (undocumented)
export const MATH_INLINE: (formula: string) => NodeType<'mathInline'>;

// @public (undocumented)
export const MENTION: (username: string, host: string | null, acct: string) => NodeType<'mention'>;

// @public (undocumented)
export type MfmBlock = MfmQuote | MfmSearch | MfmCodeBlock | MfmMathBlock | MfmCenter;

// @public (undocumented)
export type MfmBold = {
    type: 'bold';
    props?: Record<string, unknown>;
    children: MfmInline[];
};

// @public (undocumented)
export type MfmCenter = {
    type: 'center';
    props?: Record<string, unknown>;
    children: MfmInline[];
};

// @public (undocumented)
export type MfmCodeBlock = {
    type: 'blockCode';
    props: {
        code: string;
        lang: string | null;
    };
    children?: [];
};

// @public (undocumented)
export type MfmEmojiCode = {
    type: 'emojiCode';
    props: {
        name: string;
    };
    children?: [];
};

// @public (undocumented)
export type MfmFn = {
    type: 'fn';
    props: {
        name: string;
        args: Record<string, string | true>;
    };
    children: MfmInline[];
};

// @public (undocumented)
export type MfmHashtag = {
    type: 'hashtag';
    props: {
        hashtag: string;
    };
    children?: [];
};

// @public (undocumented)
export type MfmInline = MfmUnicodeEmoji | MfmEmojiCode | MfmBold | MfmSmall | MfmItalic | MfmStrike | MfmInlineCode | MfmMathInline | MfmMention | MfmHashtag | MfmUrl | MfmLink | MfmFn | MfmPlain | MfmText;

// @public (undocumented)
export type MfmInlineCode = {
    type: 'inlineCode';
    props: {
        code: string;
    };
    children?: [];
};

// @public (undocumented)
export type MfmItalic = {
    type: 'italic';
    props?: Record<string, unknown>;
    children: MfmInline[];
};

// @public (undocumented)
export type MfmLink = {
    type: 'link';
    props: {
        silent: boolean;
        url: string;
    };
    children: MfmInline[];
};

// @public (undocumented)
export type MfmMathBlock = {
    type: 'mathBlock';
    props: {
        formula: string;
    };
    children?: [];
};

// @public (undocumented)
export type MfmMathInline = {
    type: 'mathInline';
    props: {
        formula: string;
    };
    children?: [];
};

// @public (undocumented)
export type MfmMention = {
    type: 'mention';
    props: {
        username: string;
        host: string | null;
        acct: string;
    };
    children?: [];
};

// @public (undocumented)
export type MfmNode = MfmBlock | MfmInline;

// @public (undocumented)
export type MfmPlain = {
    type: 'plain';
    props?: Record<string, unknown>;
    children: MfmText[];
};

// @public (undocumented)
export type MfmQuote = {
    type: 'quote';
    props?: Record<string, unknown>;
    children: MfmNode[];
};

// @public (undocumented)
export type MfmSearch = {
    type: 'search';
    props: {
        query: string;
        content: string;
    };
    children?: [];
};

// @public (undocumented)
export type MfmSimpleNode = MfmUnicodeEmoji | MfmEmojiCode | MfmText | MfmPlain;

// @public (undocumented)
export type MfmSmall = {
    type: 'small';
    props?: Record<string, unknown>;
    children: MfmInline[];
};

// @public (undocumented)
export type MfmStrike = {
    type: 'strike';
    props?: Record<string, unknown>;
    children: MfmInline[];
};

// @public (undocumented)
export type MfmText = {
    type: 'text';
    props: {
        text: string;
    };
    children?: [];
};

// @public (undocumented)
export type MfmUnicodeEmoji = {
    type: 'unicodeEmoji';
    props: {
        emoji: string;
    };
    children?: [];
};

// @public (undocumented)
export type MfmUrl = {
    type: 'url';
    props: {
        url: string;
        brackets?: boolean;
    };
    children?: [];
};

// @public (undocumented)
export const N_URL: (value: string, brackets?: boolean) => NodeType<'url'>;

// @public (undocumented)
export type NodeType<T extends MfmNode['type']> = T extends 'quote' ? MfmQuote : T extends 'search' ? MfmSearch : T extends 'blockCode' ? MfmCodeBlock : T extends 'mathBlock' ? MfmMathBlock : T extends 'center' ? MfmCenter : T extends 'unicodeEmoji' ? MfmUnicodeEmoji : T extends 'emojiCode' ? MfmEmojiCode : T extends 'bold' ? MfmBold : T extends 'small' ? MfmSmall : T extends 'italic' ? MfmItalic : T extends 'strike' ? MfmStrike : T extends 'inlineCode' ? MfmInlineCode : T extends 'mathInline' ? MfmMathInline : T extends 'mention' ? MfmMention : T extends 'hashtag' ? MfmHashtag : T extends 'url' ? MfmUrl : T extends 'link' ? MfmLink : T extends 'fn' ? MfmFn : T extends 'plain' ? MfmPlain : T extends 'text' ? MfmText : never;

// @public (undocumented)
export function parse(input: string, opts?: Partial<{
    nestLimit: number;
}>): MfmNode[];

// @public (undocumented)
export function parseSimple(input: string): MfmSimpleNode[];

// @public (undocumented)
export const PLAIN: (text: string) => NodeType<'plain'>;

// @public (undocumented)
export const QUOTE: (children: MfmNode[]) => NodeType<'quote'>;

// @public (undocumented)
export const SEARCH: (query: string, content: string) => NodeType<'search'>;

// @public (undocumented)
export const SMALL: (children: MfmInline[]) => NodeType<'small'>;

// @public (undocumented)
export const STRIKE: (children: MfmInline[]) => NodeType<'strike'>;

// @public (undocumented)
export const TEXT: (value: string) => NodeType<'text'>;

// @public (undocumented)
function toString_2(tree: MfmNode[]): string;

// @public (undocumented)
function toString_2(node: MfmNode): string;
export { toString_2 as toString }

// @public (undocumented)
export const UNI_EMOJI: (value: string) => NodeType<'unicodeEmoji'>;

// (No @packageDocumentation comment for this package)

```