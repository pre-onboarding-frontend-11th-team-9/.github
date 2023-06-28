# 코드 컨벤션

## 기본 준수 사항

- TS 사용
- Prettier, ESLint, Husky 사용

## 세부 사항

### 컴포넌트

컴포넌트는 다음의 양식으로 제작한다.

```tsx
type ComponentProps = {
  foo: string;
};

export const Component = ({ foo }: ComponentProps) => {
  return <>{foo}</>;
};
```

- interface 대신 type 사용
- function 대신 Arrow function
- `~Props` naming

### Handler

Handler는 다음의 양식으로 제작한다.

```tsx
const handleModifyButtonClick = (e: React.MouseEvent<HTMLButtonElement>) => {
  e.preventDefault();
  setIsModifyMode(true);
};
```

- `handle~` naming
- 이벤트 변수 event 대신 e 사용

### Hook

- 불필요한 useCallback & useMemo는 일단 사용하지 않는다.
- 불필요한 useEffect는 사용하지 않는다. 예) 파생 상태

### 기타
