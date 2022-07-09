# skill-tree
# python
# How many numbers are in the skill tree in order of skill? 스킬트리안에 있는 수들중에 스킬의 순으로 적혀있는 수는 몇개인가
def solution(skill, skill_trees):
    answer =0
    for i in skill_trees:
        s="" # 하나의 스킬트리를 뽑을 때마다 s 초기화
        for j in i:
            if j in skill:  # 스킬트리 중에 skill이 있다면 s에 추가
                s+=j
        if skill[:len(s)]==s:  # 만든 s를 기준으로 skill과 같다면 answer += 1
                answer+=1
    return answer
print(solution("CBD", ["BACDE", "CBADF", "AECB", "BDA"]))
#result--> 2
