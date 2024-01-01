# from random import randint

def draw_lottery():
    # 10% 확률로 경고 빼기
    if randint(1, 100) <= 10:
        return "경고 빼기!"
    # 30% 확률로 500머니
    elif randint(1, 100) <= 30:
        return "500머니 획득!"
    # 60% 확률로 10머니
    else:
        return "10머니 획득!"

# 카카오톡 봇에서 사용자의 입력을 받아서 처리하는 함수
def process_user_input(user_input):
    if user_input == "!뽑기":
        result = draw_lottery()
        return result
    else:
        return "지원하지 않는 명령어입니다."

# 테스트용 예시
input_command = "!뽑기"
result = process_user_input(input_command)
print(result)
